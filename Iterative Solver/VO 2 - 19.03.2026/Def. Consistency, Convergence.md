The linear fixed point method is
- **consistent**, if
  $$

  \forall x \in \mathbb{K}^n:\quad x = \Phi(Ax, x),

  $$

  i.e., each solution $x$ of $Ax = b$ is a fixed point of the corresponding iteration.
- **convergent**, if
  $$

  \forall b \in \mathbb{K}^n\ \exists x^\ast \in \mathbb{K}^n\ \forall x_0 \in \mathbb{K}^n,\quad

  x_{k+1} := \Phi(b, x_k):\quad x^\ast = \lim_k x_k.

  $$
**KNOWN:** Convergence yields that
$$

x^\ast = \Phi(b, x^\ast),

$$
i.e., each limit is a fixed point (if the limit exists).