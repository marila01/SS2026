---
aliases:
  - "Example: Spectral Norm"
  - "Example: Spectral Norm"
  - "Example: Spectral Norm"
---
# Example: $\lVert A\rVert_2 = \sqrt{\rho(A^H A)}$ (so-called spectral norm)

Let $\{v_1,\dots,v_n\} \subseteq \mathbb{K}^n$ be an orthonormal basis with

$$
A^H A v_j = d_j v_j
$$

and

$$
|d_1| \le \cdots \le |d_n| = \rho(A^H A).
$$

Write

$$
x = \sum_{j=1}^n \mu_j v_j
$$

and note that

$$
\lVert x\rVert_2 := \left(\sum_{j=1}^n |x_j|^2\right)^{1/2} = \left(\sum_{j=1}^n |\mu_j|^2\right)^{1/2}.
$$

Indeed,

$$
\lVert x\rVert_2^2 = (x,x)_2 = \left(\sum_j \mu_j v_j, \sum_k \mu_k v_k\right)_2 = \sum_{j,k} \overline{\mu_j}\mu_k (v_j,v_k)_2 = \sum_j |\mu_j|^2.
$$

Similarly, we get

$$
\lVert Ax\rVert_2^2 = (Ax,Ax)_2 = (A^H A x, x)_2 = \sum_{j,k} \overline{\mu_j}\mu_k (A^H A v_j, v_k)_2 = \sum_j |\mu_j|^2 d_j
$$

and thus

$$
\lVert Ax\rVert_2^2 \le |d_n| \sum_j |\mu_j|^2 = \rho(A^H A)\,\lVert x\rVert_2^2.
$$

This proves

$$
\lVert A\rVert_2^2 \le \rho(A^H A).
$$

For $x = v_n$, we even see equality.
