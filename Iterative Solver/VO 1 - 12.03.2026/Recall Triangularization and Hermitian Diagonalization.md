---
aliases:
  - "Recall: Triangularization and Hermitian Diagonalization"
---
## Recall

- Each matrix $A \in \mathbb{K}^{n\times n}$ is **triangularizable over $\mathbb{C}$**, i.e., there exists a regular matrix $T \in \mathbb{C}^{n\times n}$ and an upper triangular matrix $U \in \mathbb{C}^{n\times n}$ such that
  $$
  U = T^{-1}AT
  $$
  with $U_{ij} = 0$ for $i>j$.
- The diagonal elements $d_j := U_{jj}$ are the eigenvalues of $U$ and $A$, i.e., there exist $v_j \in \mathbb{C}^{n}\setminus\{0\}$ such that
  $$
  Av_j = d_j v_j.
  $$
- Each Hermitian matrix
  $$
  A = A^{H} := \overline{A}^{\,T} \in \mathbb{K}^{n\times n}
  $$
  is **diagonalizable over $\mathbb{K}$**, i.e., there exists a regular (and even orthogonal/unitary) matrix $Q \in \mathbb{K}^{n\times n}$ and a diagonal matrix $D \in \mathbb{R}^{n\times n}$ such that
  $$
  D = Q^{H} A Q
  $$
  with $D_{ij}=0$ for $i\ne j$ and $Q^{H} Q = I$.
- The diagonal elements $d_j := D_{jj} \in \mathbb{R}$ are the eigenvalues of $D$ and $A$. Moreover, the columns $v_j$ of $Q$ are the eigenvectors of $A$, and $\{v_1,\dots,v_n\} \subseteq \mathbb{K}^{n}$ is an orthonormal basis of $\mathbb{K}^{n}$ with respect to the Euclidean scalar product
  $$
  (x,y)_2 := x^{H} y
  $$
  for $x,y \in \mathbb{K}^{n}$.
