-
- **定理**(Universal Approximation Theorem). 令 $\phi$ 是非常数、有界、单调递增的连续函数，$\mathcal{J}_D$ 是 $D$ 维的单位超立方体 $[0,1]^D$，$C(\mathcal{J}_D)$ 是定义在 $\mathcal{J}_D$ 上的连续函数集合。对于任意给定的 $f \in C(\mathcal{J}_D)$，存在整数 $M$，以及 $v_m, b_m \in \mathbb{R}$ 以及 $\mathbf{w}_m \in \mathbb{R}^D$，$m = 1,2,\cdots,M$，定义

$$ F(x) = \sum\limits_{m = 1}^M v_m\phi(\mathbf{w}_m^T x + b_m), $$

满足

$$ |F(x) - f(x)| < \epsilon, \quad \forall x \in \mathcal{J}_D, $$

其中 $\epsilon > 0$ 是个很小的正数。

-
