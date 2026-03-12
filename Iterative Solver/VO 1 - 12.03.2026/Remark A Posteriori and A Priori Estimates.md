---
aliases:
  - "Remark: A Posteriori and A Priori Estimates"
  - "Remark: A Posteriori and A Priori Estimates"
---
# Remark

- The first estimate in (iii) and the estimate in (iv) are so-called **a-posteriori error estimates**: We can control the error from above and below from the computed iterates $x_k, x_{k+1}$, even if we do not know the exact solution $x^*$.
- The estimate
  $$
  \lVert x^*-x_{k+1}\rVert \le \frac{q^{k+1}}{1-q}\,\lVert x_1-x_0\rVert
  $$
  is an **a-priori error estimate**: Before computing $x_{k+1}$ and only by knowledge of $q, x_0, x_1$, we know how many iterations it needs at most to drive the error below a prescribed tolerance.
