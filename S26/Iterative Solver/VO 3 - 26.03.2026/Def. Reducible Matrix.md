---
aliases:
  - "Def.: Reducible Matrix"
---
$A \in \mathbb{K}^n$ is called **reducible** $\iff$ $\exists J,K \subset \{ 1,\dots,n \}$ with $\emptyset\neq J,K,J \cap K$, $J \cup K=\{ 1,\dots ,n \}$ and $\forall j \in J,k\in K:A_{jk}=0$.

If you want to solve $Ax=b$. For $j \in J$: $b_{j}=\sum_{\ell=1}^nA_{j\ell}x_{\ell}=\sum_{\ell \in J}A_{j \ell}x_{\ell}$. This is a $|J|\times|J|$ linear system (smaller).
This is similar to transforming $A$ to block-matrix-form 
$$
A = \begin{pmatrix}
A_{1} & 0 \\
A_{2} & A_{3}
\end{pmatrix}.
$$