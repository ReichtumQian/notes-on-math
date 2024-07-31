-
- ## 梯形公式
- **定义**(梯形公式). 梯形公式的计算格式为
  
  $$ I^T(f) = \frac{b - a}{2}[f(a) + f(b)]. $$
- **定理**(梯形公式精度). 给定 $f \in C^2[a,b]$，权重函数 $\rho(x) \equiv 1$，梯度公式的余项为
  
  $$ \exists \zeta \in [a,b] ~ \mathrm{s.t.} ~ E^T(f) = I(f) - I^T(f) = - \frac{(b - a)^3}{12}f^{\prime\prime}(\zeta). $$
- **证明**. 根据多项式插值 Cauchy 余项可知
  
  $$ f(x) - p_1(f;x) = \frac{f^{\prime\prime}(\xi(x))}{2} (x - a)(x - b), $$
  
  因此有
  
  $$
  \begin{align*}
  E^T(f) &= - \int_a^b \frac{f^{\prime\prime}(\xi(x))}{2}(x - a)(x - b)\mathrm{d} x\\
  &= - \frac{f^{\prime\prime}(\zeta)}{2} \int_a^b (x-a)(x-b)\mathrm{d} x = - \frac{(b-a)^3}{12}f^{\prime\prime}(\zeta),
  \end{align*}
  $$
  
  其中第二个等号使用了 [[积分第一中值定理]]。
-
-
-
-
-
-