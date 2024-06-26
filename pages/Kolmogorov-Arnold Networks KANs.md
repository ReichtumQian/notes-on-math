-
- `KANs` 是基于 [[Kolmogorov-Arnold 表示定理]] 的神经网络，由于 Kolmogorov-Arnold 表示定理中的表示公式
  
  $$ f(\mathbf{x}) = f(x_1,\cdots,x_n) = \sum\limits_{q = 1}^{2n+1} \Phi_q \left( \sum\limits_{p = 1}^n \phi_{q,p}(x_p) \right) $$
  
  中仅含单变量函数，可用 B-spline 对单变量函数进行拟合，并使用神经网络学习 B-spline 中的参数。
- ![image.png](../assets/image_1719643618104_0.png)
- 注意：上图中加粗的 $\bm \Phi$ 和前面表示定理中的 $\Phi$ 不一样。
- ## KA 表示定理的网络表示
- 根据 KA 表示定理，只需要两层（有两层可学习的参数，一般 Input 算第 0 层）就可以拟合一个函数，对于数据为 $n$ 维向量，激活函数定义于边上
	- $\phi_{\ell,i,j}$：表示第 $\ell$ 层，第 $i$ 个变量的第 $j$ 个激活函数。$x_{\ell,j}$ 表示第 $\ell$ 层第 $j$ 个神经元。
	- 第一层表示公式中的 $\phi_{q,p}, q = j, p = i$，满足 $i = 1,2,\cdots,n$ 以及 $j = 1,2,\cdots,2n+1$。
	- 第二层表示公式中的 $\Phi_q$。
	- 激活函数都使用 B-Spline 表示。
- 如图所示：每个变量输入后第一层先计算 $\phi_{q,p}(x_p)$，然后求和得到 $\sum_{p = 1}^n \phi_{q,p}(x_p)$，再通过 $\Phi_q$ 映射，最后求和得到目标函数。（注意图中的方框表示边中的映射，并非神经元）
- ![image.png](../assets/image_1719645400141_0.png)
- ## KANs
- 虽然 KA 表示定理只需要两层网络就可以表达，但是这种表达不够深因而缺乏表达能力，KANs 对该表示做了一些修改。
- 符号：假设共 $L$ 层（编号从 $0$ 开始）；各层网络分别有 $n_0,\cdots,n_L$ 个神经元；用 $(\ell,i)$ 表示第 $\ell$ 层第 $i$ 个神经元；$\phi_{\ell,i,j}$ 表示 $(\ell,j)$ 与 $(\ell+1, i)$ 的边
- KAN 层：类似于 KA 表示定理的两层网络格式，第 $\ell+1$ 层与第 $\ell$ 层的关系为
  
  $$ x_{\ell+1,j} = \sum\limits_{i = 1}^{n_{\ell}}\phi_{\ell,i,j}(x_{\ell,i}), \quad j = 1,\cdots,n_{\ell+1}, $$
  
  写为矩阵形式即
  
  $$ \mathbf{x}_{\ell + 1} = 
  \left[\begin{array}{cccc}
  \phi_{\ell,1,1}(\cdot) & \phi_{\ell,1,2}(\cdot) & \cdots & \phi_{\ell,1,n_{\ell}}(\cdot)\\
  \phi_{\ell,2,1}(\cdot) & \phi_{\ell,2,2}(\cdot) & \cdots & \phi_{\ell,2,n_{\ell}}(\cdot)\\
  \vdots & \vdots &&\vdots\\
  \phi_{\ell,n_{\ell+1},1}(\cdot) & \phi_{\ell,n_{\ell+1},2}(\cdot) & \cdots & \phi_{\ell,n_{\ell+1},n_{\ell}}(\cdot)
  \end{array}  \right]\mathbf{x}_{\ell}.
  $$
- KAN 的整体效果：为了与 KA 表示定理做对比，这里列出 KAN 网络的效果

$$ f(\mathbf{x})=\sum_{i_{L-1}=1}^{n_{L-1}}\phi_{L-1,i_{L},i_{L-1}}\left(\sum_{i_{L-2}=1}^{n_{L-2}}\cdots\left(\sum_{i_{2}=1}^{n_{2}}\phi_{2,i_{3},i_{2}}\left(\sum_{i_{1}=1}^{n_{1}}\phi_{1,i_{2},i_{1}}\left(\sum_{i_{0}=1}^{n_{0}}\phi_{0,i_{1},i_{0}}(x_{i_{0}})\right)\right)\right)\cdots\right).$$

-
-
-
-
- ## 参考文献
- Liu, Ziming, et al. "Kan: Kolmogorov-arnold networks." *arXiv preprint arXiv:2404.19756* (2024).
-
-
