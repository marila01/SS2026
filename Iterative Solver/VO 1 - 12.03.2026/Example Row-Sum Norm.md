---
aliases:
  - "Example: Row-Sum Norm"
---
# Example: $\lVert\cdot\rVert_\infty$ induces the row-sum norm

We consider

$$
\lVert x\rVert_\infty := \max_{j=1,\dots,n} |x_j|
$$

on $\mathbb{K}^n$.

For $A \in \mathbb{K}^{n\times n}$, it follows that

$$
\lVert Ax\rVert_\infty
=
\max_j \left|\sum_k A_{jk}x_k\right|
\le
\max_j \sum_k |A_{jk}|\,|x_k|
\le
\max_j \sum_k |A_{jk}|\,\lVert x\rVert_\infty.
$$

Hence,

$$
\lVert A\rVert_\infty \le \max_j \sum_k |A_{jk}|,
$$

the so-called **row-sum norm** of $A$.

To see equality, pick an index $j_0 \in \{1,\dots,n\}$ with maximal value, and define

$$
x_k := \operatorname{sign}(A_{j_0k}),
$$

i.e., $|x_k|=1$ and $A_{j_0k}x_k = |A_{j_0k}|$.

With this, one has $\lVert x\rVert_\infty = 1$ and equality.
