---
aliases:
  - "Lemma: diagonally dominant + irreducible = regular"
---
Let $A \in \mathbb{K}^n$ be diagonally dominant and irreducible (=not reducible), then $A$ is regular.

##### Proof:
Let $x \in \mathbb{K}^n\setminus \{ 0 \}$ such that $Ax=0$.
Then $A-\text{diag}(A)=-\text{diag}(A)$.
Taking absolute values in every component yields (As in [[Lemma (Strictly diagonal dominant Matrix is regular)]]):
$$\forall j = 1, \dots, n: |A_{jj}||x_{j}|\leq \sum_{i=1,i\neq j}^n|A_{ji}||x_{i}|$$
Then $\emptyset\neq J =\{ j : |x_{j}|=||x||_{\infty} \}$, $K=\{ k : |x_{k}|<||x||_{\infty} \}, J \cap K=\emptyset, J \cup K = \{ 1,\dots,n \}$.
If $K= \emptyset$, then $\forall j=1,\dots,n:|x_{j}|=||x||_{\infty}$.
So this would yield
$$\forall j = 1,\dots,n: A_{jj}\leq \sum_{i=1,i\neq j}^n|A_{ji}|$$
This would contradict the diagonal dominance.
So we get $K\neq \emptyset$.
This implies, that $\exists j \in J,k\in K$ such that $A_{jk}\neq 0$ and
$$
|A_{j j}|\leq \sum_{\ell=1,\ell\neq j}^n |A_{j\ell}| \frac{|x_{\ell}|}{|x_{j}|}<\sum_{\ell=1,\ell \neq j}^n|A_{j\ell}|
$$
This contradicts the diagonal dominance.
So $x= 0 \implies \text{ker}A=\{ 0 \}$.