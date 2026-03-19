Let $A \in \mathbb{K}^{n \times n}$ be strictly diagonal dominant and hence regular.
Let
$$

\Pi^{(J)} := -D^{-1}(A-D),\qquad

\Pi^{(GS)} := -(D+L)^{-1}U

$$
be the iteration matrices of Jacobi and Gauss-Seidel iteration, respectively.
Then,
$$

\|\Pi^{(GS)}\|_\infty \le \|\Pi^{(J)}\|_\infty < 1

$$
and hence $\rho(\Pi^{(GS)})<1$ as well as $\rho(\Pi^{(J)})<1$, i.e., Jacobi and Gauss-Seidel iteration guarantee convergence.

##### Proof:
1. We show that $\|\Pi^{(J)}\|_\infty < 1$.
   Recall that
   $$
   \Pi^{(J)} = -D^{-1}(A-D),
   $$
   i.e.,
   $$
   \Pi^{(J)}_{jk} =
   \begin{cases}
   0 & \text{if } j=k,\\
   \dfrac{A_{jk}}{A_{jj}} & \text{if } j\ne k.
   \end{cases}
   $$ $$\|\Pi^{(J)}\|_\infty=\max_{j=1,\dots,n}\sum_{k=1}^n |\Pi^{(J)}_{jk}|= \max_j \sum_{k\ne j}\left|\frac{A_{jk}}{A_{jj}}\right|
 < 1
 $$
   by strict diagonal dominance.

For this proof, let us consider $\le$ and $|\,\cdot\,|$ componentwise for all matrix entries.

2. $D^{-1}(L+D)=I+D^{-1}L$ and $\rho(D^{-1}L)=0$.
   The Neumann series proves  $$

   [D^{-1}(L+D)]^{-1}

   = I - (-D^{-1}L)

   = \sum_{k=0}^\infty (-D^{-1}L)^k.

   $$
   Taking $|\,\cdot\,|$, this yields
   $$

   |[D^{-1}(L+D)]^{-1}|

   \le

   \sum_{k=0}^\infty |D^{-1}L|^k

   =

   (I-|D^{-1}L|)^{-1}.

   $$
3. $\Pi^{(J)} = -D^{-1}(A-D) = -D^{-1}(L+U)$
   $$

   \Rightarrow\quad

   |\Pi^{(J)}|

   =

   |D^{-1}L| + |D^{-1}U|,

   $$
   since matrix pattern of $L,U$ are disjoint and $D^{-1}$ is diagonal (i.e., scaling of rows). $$

   \Rightarrow\quad

   |D^{-1}U|

   =

   (|\Pi^{(J)}|-I) + (I-|D^{-1}L|).

   $$
4. After these preparations, we aim to conclude the proof.
   Recall that
$$

   \Pi^{(GS)} = -(D+L)^{-1}U.

   $$
   $$

   |\Pi^{(GS)}|

   =

   |(D+L)^{-1}U|

   =

   |[D^{-1}(D+L)]^{-1}D^{-1}U|

   \le

   |[D^{-1}(D+L)]^{-1}|\ |D^{-1}U|

   $$
   $$

   \le

   |(I-D^{-1}L)^{-1}|\ |D^{-1}U|

   =

   (I-|D^{-1}L|)^{-1}|D^{-1}U|

   $$
   $$

   =

   (I-|D^{-1}L|)^{-1}\big((|\Pi^{(J)}|-I) + (I-|D^{-1}L|)\big)

   $$
   $$

   =

   (I-|D^{-1}L|)^{-1}(|\Pi^{(J)}|-I) + I.

   $$

Let $e=(1,\dots,1)^T \in \mathbb{K}^n$.

$$

\Rightarrow\quad

|\Pi^{(GS)}|e

\le

(I-|D^{-1}L|)^{-1}(|\Pi^{(J)}|(e-e)) + e

$$

$$

=

\sum_{k=0}^\infty |D^{-1}L|^k \big((\|\Pi^{(J)}\|_\infty - 1)e\big) + e

$$

$$

\le

(\|\Pi^{(J)}\|_\infty - 1)e + e

=

\|\Pi^{(J)}\|_\infty e.

$$

$$

\Rightarrow\quad

\|\Pi^{(GS)}\|_\infty

=

\||\Pi^{(GS)}|e\|_\infty

\le

\|\Pi^{(J)}\|_\infty \|e\|_\infty

=

\|\Pi^{(J)}\|_\infty \cdot 1.

$$

  

