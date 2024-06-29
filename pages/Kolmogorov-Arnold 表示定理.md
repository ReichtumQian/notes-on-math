-
- **定理**(Kolmogorov-Arnold Representation Theorem). 若 $f: [0,1]^n \rightarrow \mathbb{R}$ 是多元连续函数，则其可以被写成单变量函数的组合
  
  $$ f(\mathbf{x}) = f(x_1,\cdots,x_n) = \sum\limits_{q = 1}^{2n+1} \Phi_q \left( \sum\limits_{p = 1}^n \phi_{q,p}(x_p) \right), $$
  
  其中 $\phi_{q,p}:[0,1] \rightarrow \mathbb{R}, \Phi_q: \mathbb{R} \rightarrow \mathbb{R}$ 是一些适当的单变量连续函数。
- #+BEGIN_NOTE
  上述 $q = 1,2,\cdots,2n+1$ 是被严格证明的，至少需要 $2n+1$ 个函数才能逼近。体现在神经网络中，即至少需要 $2n+1$ 个隐藏层
  #+END_NOTE
-