---
aliases:
  - "Remark: Error Propagation"
---
## Remark: Error Propagation

The lemma states that $\operatorname{cond}_{\lVert\cdot\rVert}(A)$ is the worst-case factor for error propagation if the computer uses a rounded $\tilde{b}$ instead of the exact $b$, under the idealistic assumption that computer arithmetic is exact.

Recall that direct solvers like Gaussian elimination factorize the matrix $A = LU$ and solve sequentially with $L$ and $U$. Unfortunately, this can lead to error propagation with factor

$$
\operatorname{cond}_{\lVert\cdot\rVert}(L)\,\operatorname{cond}_{\lVert\cdot\rVert}(U)
\ge
\operatorname{cond}_{\lVert\cdot\rVert}(A),
$$

where $\operatorname{cond}_{\lVert\cdot\rVert}(A)$ can be much smaller.
