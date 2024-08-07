-
- **定义**(Jacobi 迭代). 线性方程组 $Ax = b$ 的系数矩阵分解为 $A = D - L - U$，其中 $D$ 是 $A$ 对角线元素组成的矩阵，$L, U$ 分别是 $A$ 下、上三角取负形成的矩阵，则 Jacobi 迭代定义为

$$ x_k = D^{-1}(L+U)x_{k-1} + D^{-1} b, $$

其中 $x_k$ 是 $n \times 1$ 的向量，用于逼近真实解 $x$。

-
-
