
---

  

**COROLLARY:** Let $A \in \mathbb{K}^{n \times n}$ such that $A^T$ is strictly diagonal dominant.

  

Then, $A$ is regular, the Jacobi iteration is well-defined, and convergent **for $A$**.

  

**Proof:**

  

According to $0 \ne \det(A^T)=\det(A)$, $A$ is regular.

  

Since $A^T$ is strictly diagonal dominant, $A_{jj}^T \ne 0$ for all $j=1,\dots,n$.

Therefore, $\Pi^{(J)}$ is well-defined.

  

Recall that

  

- $\|B\|_\infty = \max_j \sum_k |B_{jk}|$  (row-sum norm),

- $\|B\|_1 = \max_k \sum_j |B_{jk}|$  (column-sum norm).

  

Hence,

  

$$

\rho(\Pi^{(J)}) \le \|\Pi^{(J)}\|_1

= \|(\Pi^{(J)})^T\|_\infty

= \|(A^T-D)D^{-1}\|_\infty

< 1

$$

  

as in the theorem.