Let $A$ be diagonally dominant and irreducible. Then JI and GSI are convergent.

##### Proof:
**Jacobi:**
We need to show $\rho(M^{(J)})<1$ with $M^{(J)}=D^{-1}(A-D)$.

$M=M^{(J)}-\lambda I, |\lambda|\geq 1$. We need to show, that $M$ is regular.
Because scaling with something $\geq 1$ does not produce any more zeros, we get:
$A$ is irreducible $\implies A-D$ is irreducible $\implies M^{(J)}$ is irreducible $\implies M$ is irreducible.
Then
$$
\sum_{k=1,j\neq k}^n|M_{jk}|=\sum_{k=1,j\neq k}^n |M_{jk}^{(J)}|=\sum_{k=1,j\neq k} \frac{|A_{jk}|}{|A_{jj}|} \stackrel{\text{d.d.}}{\leq} 1\leq |\lambda| \stackrel{M_{ii}=0}{=}|M_{jj}|
$$
Because this has to be strict for $j$ ([[Def. Diagonally Dominant Matrix]]), we get that $M$ is diagonally dominant and therefore regular by [[Lemma diagonally dominant + irreducible = regular]].

**Gauss-Seidel:**
$M^{(GS)}=-(L+D)^{-1}U$. Same strategy as for Jacobi.
$M:=M^{(GS)}-\lambda I,|\lambda|\geq 1$.
$M$ regular $\iff$ $-(L+D)M=-(L+D)(-(L+D)^{-1}U-\lambda I)=U+\lambda L+\lambda D=:\tilde{M}$.
$A$ is irreducible with $A=L+D+U$ $\implies U+\lambda L+\lambda D$ irreducible $\implies-(L+D)M$ irreducible.
$$
\sum_{k=1,j\neq k}^n|\tilde{M}_{jk}|=\sum_{k=j+1}^n |A_{jk}|+|\lambda|\sum_{k=1}^{j-1}|A_{jk}|\leq |\lambda|\left( \sum_{k=1,k\neq j}^n |A_{jk}| \right) \stackrel{\text{d.d.}}{\leq} |\lambda||A_{jj}|=|\tilde{M}_{jj}|
$$
and for one $j$, this is strict, so $\tilde{M}$ is diagonally dominant.
By [[Lemma diagonally dominant + irreducible = regular]] $\tilde{M}$ is regular, so $M$ is regular.