---
aliases:
  - "Example (backward Gauss-Seidel iteration):"
---
$$

A = (D+U) + L,\qquad

G := D+U,\qquad

H := -L.

$$
$$
x_i^{k+1}
=
x_i^k
+
\frac{1}{A_{ii}}
\left(
b_i
-
\sum_{j=1}^{i-1} A_{ij}x_j^{k}
-
\sum_{j=i}^{n} A_{ij}x_j^{k+1}
\right)
\qquad \text{for all } i=1,\dots,n.
$$

  