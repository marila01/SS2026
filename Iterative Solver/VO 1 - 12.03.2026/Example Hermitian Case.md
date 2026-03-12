---
aliases:
  - "Example: Hermitian Case"
  - "Example: Hermitian Case"
  - "Example: Hermitian Case"
---
# Example: $\lVert A\rVert_2 = \rho(A)$ for $A = A^H$

Let $\{v_1,\dots,v_n\} \subseteq \mathbb{K}^n$ be an orthonormal basis with

$$
Av_j = d_j v_j
$$

and

$$
|d_1| \le \cdots \le |d_n| = \rho(A).
$$

Write

$$
x = \sum_j \mu_j v_j.
$$

Then,

$$
\lVert Ax\rVert_2^2 = (Ax,Ax)_2 = \sum_{j,k} \overline{\mu_j}\mu_k (Av_j, Av_k)_2 = \sum_j |\mu_j|^2 d_j^2 \le |d_n|^2 \sum_j |\mu_j|^2 = \rho(A)^2 \lVert x\rVert_2^2.
$$

This proves

$$
\lVert A\rVert_2^2 \le \rho(A)^2.
$$

For $x = v_n$, we again see equality.
