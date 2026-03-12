---
aliases:
  - "Example: Column-Sum Norm"
---
## Example: $\lVert\cdot\rVert_1$ induces the column-sum norm

We consider

$$
\lVert x\rVert_1 := \sum_{j=1}^{n} |x_j|
$$

on $\mathbb{K}^{n}$.

For $A \in \mathbb{K}^{n\times n}$, it follows that

$$
\lVert Ax\rVert_1
=
\sum_{j=1}^{n} |(Ax)_j|
=
\sum_{j=1}^{n} \left|\sum_{k=1}^{n} A_{jk}x_k\right|
\le
\sum_k \left(\sum_j |A_{jk}|\right)|x_k|
\le
\left(\max_k \sum_j |A_{jk}|\right) \sum_k |x_k|.
$$

This yields

$$
\lVert A\rVert_1 \le \max_k \sum_j |A_{jk}|,
$$

the so-called **column-sum norm** of $A$.

To see equality, fix the index $k_0 \in \{1,\dots,n\}$ such that

$$
\sum_{j=1}^{n} |A_{jk_0}| = \max_k \sum_j |A_{jk}|.
$$

Choose $x = e_{k_0}$, the $k_0$-th unit vector.

Then $\lVert x\rVert_1 = 1$ and

$$
\sum_j \left|\sum_k A_{jk}x_k\right| = \sum_j |A_{jk_0}| = \max_k \sum_j |A_{jk}|.
$$
