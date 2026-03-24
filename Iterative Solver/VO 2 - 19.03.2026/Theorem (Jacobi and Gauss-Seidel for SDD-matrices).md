Let $A \in \mathbb{K}^{n \times n}$ be strictly diagonal dominant and hence regular.
Let
$$

M^{(J)} := -D^{-1}(A-D),\qquad

M^{(GS)} := -(D+L)^{-1}U

$$
be the iteration matrices of Jacobi and Gauss-Seidel iteration, respectively.
Then,
$$

\|M^{(GS)}\|_\infty \le \|M^{(J)}\|_\infty < 1

$$
and hence $\rho(M^{(GS)})<1$ as well as $\rho(M^{(J)})<1$, i.e., Jacobi and Gauss-Seidel iteration guarantee convergence.

##### Proof:
1. We show that $\|M^{(J)}\|_\infty < 1$.
   Recall that  
$$M^{(J)} = -D^{-1}(A-D),$$
   i.e., 
$$ M^{(J)}_{jk} =
\begin{cases}
0 & \text{if } j=k,\\
\dfrac{A_{jk}}{A_{jj}} & \text{if } j\ne k.
\end{cases}$$

$$
\|M^{(J)}\|_\infty=\max_{j=1,\dots,n}\sum_{k=1}^n |M^{(J)}_{jk}|= \max_j \sum_{k\ne j}\left|\frac{A_{jk}}{A_{jj}}\right|
 < 1
$$
   by strict diagonal dominance.

For this proof, let us consider $\le$ and $|\,\cdot\,|$ componentwise for all matrix entries.

2. $D^{-1}(L+D)=I+D^{-1}L$ and $\rho(D^{-1}L)=0$.
   The Neumann series proves  

$$
[D^{-1}(L+D)]^{-1}

= I - (-D^{-1}L)

= \sum_{k=0}^\infty (-D^{-1}L)^k.
$$
   Taking $|\,\cdot\,|$, this yields

$$
|[D^{-1}(L+D)]^{-1}| \le \sum_{k=0}^\infty |D^{-1}L|^k =(I-|D^{-1}L|)^{-1}.$$ $$M^{(J)} = -D^{-1}(A-D) = -D^{-1}(L+U)$$
 $$
\Rightarrow\quad
|M^{(J)}|
=
|D^{-1}L| + |D^{-1}U|,
$$
   since matrix pattern of $L,U$ are disjoint and $D^{-1}$ is diagonal (i.e., scaling of rows). $$
\Rightarrow\quad
|D^{-1}U|
=
(|M^{(J)}|-I) + (I-|D^{-1}L|).
$$
5. After these preparations, we aim to conclude the proof.
   Recall that
$$
M^{(GS)} = -(D+L)^{-1}U.
$$
$$
|M^{(GS)}|
=
|(D+L)^{-1}U|
=
|[D^{-1}(D+L)]^{-1}D^{-1}U|
\le
|[D^{-1}(D+L)]^{-1}|\ |D^{-1}U|
$$
$$\le|(I-D^{-1}L)^{-1}|\ |D^{-1}U|=(I-|D^{-1}L|)^{-1}|D^{-1}U|$$
$$=(I-|D^{-1}L|)^{-1}\big((|M^{(J)}|-I) + (I-|D^{-1}L|)\big)$$
$$=(I-|D^{-1}L|)^{-1}(|M^{(J)}|-I) + I.$$

Let $e=(1,\dots,1)^T \in \mathbb{K}^n$.

$$

\Rightarrow\quad

|M^{(GS)}|e

\le

(I-|D^{-1}L|)^{-1}(|M^{(J)}|(e-e)) + e

$$

$$

=

\sum_{k=0}^\infty |D^{-1}L|^k \big((\|M^{(J)}\|_\infty - 1)e\big) + e

$$

$$

\le

(\|M^{(J)}\|_\infty - 1)e + e

=

\|M^{(J)}\|_\infty e.

$$

$$

\Rightarrow\quad

\|M^{(GS)}\|_\infty

=

\||M^{(GS)}|e\|_\infty

\le

\|M^{(J)}\|_\infty \|e\|_\infty

=

\|M^{(J)}\|_\infty \cdot 1.

$$

  

