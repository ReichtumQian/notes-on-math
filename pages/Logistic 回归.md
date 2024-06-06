- Logistic Regression 回归是 [[机器学习]] 中的一种学习算法
- **定义**(Logistic Regression). 给定 $M$ 个样本 $(x^{(1)}, y^{(1)}),\cdots, (x^{(M)}, y^{(M)})$，其中 $y^{(i)} \in \{0,1\}$， 拟合出如下 $y$ 与 $x$ 之间的关系
  
  $$ h_{\theta} = \frac{1}{1 + e^{- \theta^T x}}, $$
  
  $h_{\theta}$ 是 [[Sigmoid 函数]]。
-
- ## 极大似然估计
- 类似于 [[线性回归]]，我们首先要明确怎样的 $\theta$ 能够最符合要求，即进行最大 [[似然函数]] 估计。
- **引理**. Logistic Regression 中满足
  
  $$ P(y|x; \theta) = [h_{\theta}(x)]^y [(1 - h_{\theta}(x))]^{1-y} $$
  
  **证明**. 由于 $y \in \{0, 1\}$，因此 $y = 0$ 时 $P(y|x;\theta) = 1 - h_{\theta}(x)$， $y = 1$ 时 $P(y|x;\theta) = h_{\theta}(x)$ 满足条件。
- **定理**. Logistic Regression 中取 $\theta$ 满足最大化对数似然
  
  $$
  \ell(\theta) = \sum\limits_{i = 1}^M y^{(i)}\log h_{\theta}(x^{(i)}) + (1 - y^{(i)}) \log (1 - h_{\theta}(x^{(i)}))
  $$
  
  **证明**. 计算 $\mathcal{L}(\theta)$：
  
  $$
  \begin{align*}
  \mathcal{L}(\theta) = & \prod \limits_{i = 1}^M P(y^{(i)} | x^{(i)}; \theta)\\
  &= \prod\limits_{i = 1}^M h_{\theta}(x^{(i)})^{y^{(i)}} \left( 1 - h_{\theta}(x^{(i)})^{1 - y^{(i)}} \right)
  \end{align*}
  $$
  
  取对数即可得到结论。
- 一般使用梯度上升法求解 Logistic Regression 的对数似然。
-
-
-
-
-