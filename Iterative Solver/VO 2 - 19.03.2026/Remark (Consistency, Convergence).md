There are different ways to write/think the linear fixed point iteration
$$

x_{k+1} := \Phi(b, x_k) = \Pi x_k + Nb:

$$
**(a)** With consistency, we get $I = \Pi + NA$ and hence $\Pi = I - NA$
$$

\Rightarrow\quad x_{k+1} = x_k + N(b-Ax_k)

$$
Richardson-type update formulation.

**(b)**
$$

N^{-1}(x_{k+1}-x_k) = b-Ax_k

$$
solving for update as for Newton.

  