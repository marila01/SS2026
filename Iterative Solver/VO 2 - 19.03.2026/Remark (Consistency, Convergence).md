There are different ways to write/think the linear fixed point iteration
$$x_{k+1} := \Phi(b, x_k) = M x_k + Nb:$$
**(a)** With consistency, we get $I = M + NA$ and hence $M = I - MA$
$$\Rightarrow\quad x_{k+1} = x_k + N(b-Ax_k)$$
Richardson-type update formulation, with the Preconditioner-Matrix $N$.

**(b)**
$$N^{-1}(x_{k+1}-x_k) = b-Ax_k$$
solving for update as for Newton.

  