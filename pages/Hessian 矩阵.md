-
- **定义**(Hessian 矩阵). 给定函数 $f:\mathbb{R}^n \rightarrow \mathbb{R}$，其 Hessian 矩阵为
  
  $$ \nabla^2 f(\mathbf{x}) = \mathbf{H} = \left[ 
  \begin{array}{cccc}
    \frac{\partial^2 f}{\partial x_1^2}& \frac{\partial^2 f}{\partial x_1 \partial x_2}&\cdots& \frac{\partial^2 f}{\partial x_1 \partial x_n}\\
    \frac{\partial^2 f}{\partial x_2 \partial x_1}& \frac{\partial^2 f}{\partial x_2^2}&\cdots& \frac{\partial^2 f}{\partial x_2 \partial x_n}\\
                                       \vdots&\vdots&\ddots&\vdots \\
    \frac{\partial^2 f}{\partial x_n \partial x_1}& \frac{\partial^2 f}{\partial x_n \partial x_2}&\cdots& \frac{\partial^2 f}{\partial x_n^2}
  \end{array}
  \right] $$
- #+BEGIN_TIP
  Hessian 矩阵可被视为 n 元函数的二阶导数。
  #+END_TIP
  
- ## Hessian 矩阵的性质
