- Bernstein 多项式是函数逼近中常用的基底多项式，最初由苏联数学家 Bernstein 在证明 Weierstrass 逼近定理中使用，Bernstein 多项式逼近相比于传统的插值、最小二乘算法有以下优点：
	- 数值稳定性：能够保持较好的数值稳定性，特别是在高次逼近时，不容易出现 Runge 现象；
	- 适用于任意维度：容易简单地推广至任意维度，相比于插值方便很多；
	- 非负性与凸性的保持：若被逼近函数是非负或者凸的，其 Bernstein 多项式将保持这些性质。
-
- ## 一元 Bernstein 多项式
- **定义**(一元 Bernstein 多项式). 设 $f(x): [0,1] \rightarrow \mathbb{R}$，定义
  
  $$
  B_n(f) := \sum\limits_{k = 1}^n \binom{n}{k} f \left( \frac{k}{n} \right) x^k(1 - x)^{n-k}, \quad x \in [0,1]
  $$
  
  为 $f(x)$ 的 $n$ 阶 Bernstein 多项式。
- **定理**(Bernstein 多项式逼近定理). 设 $f: [0,1] \rightarrow \mathbb{R}$ 满足 $|f(x)| \leq M$，且对于任意 $x \in [0,1]$ 有 
  
  $$B_n(f)(x) \rightarrow f(x) $$
  
  则 (1) 若 $f(x)$ 是连续的，则 $B_n(f)$ 一致收敛于 $f$；(2) 若 $f(x)$ 是连续可微的，则 $B_n^{\prime}(f)$ 一致收敛于 $f^{\prime}$。
-
- ## 多元 Bernstein 多项式
-
-
-
-