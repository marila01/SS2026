## Theorem (Gelfand)
Let $M \in \mathbb{K}^{n\times n}$ and $\|\cdot\|$ a norm on $\mathbb{K}^n$.
Then,
$$
\lim_{k\to\infty} \|M^k\|^{1/k} = \rho(M).
$$
If $\|\cdot\|$ is even a norm on $\mathbb{C}^n$ or $\sigma(M)\subset \mathbb{R}$, then
$$
\|M^k\|^{1/k} \ge \rho(M).
$$
---
##### Proof (er hat gekocht, risky business)
**1)**
If $\|\cdot\|$ is a norm on $\mathbb{C}^n$ or $\sigma(M)\subset \mathbb{R}$, let $\lambda \in \sigma(M)$ with
$$
|\lambda| = \rho(M).
$$
Let $v \in \mathbb{C}^n \setminus \{0\}$ with $Mv=\lambda v$ and $\|v\|=1$.
Note that we can choose $v \in \mathbb{K}^n \setminus \{0\}$ if $\sigma(M)\subseteq \mathbb{K}$.
Then
$$
\rho(M)=|\lambda|
=
\|\lambda^k v\|^{1/k}
=
\|M^k v\|^{1/k}
\le
\|M^k\|^{1/k}\|v\|^{1/k}
=
\|M^k\|^{1/k}.
$$
---
**2)**
Let $0<\varepsilon<\rho(M)$.
Consider
$$
M_{\pm} := \frac{1}{\rho(M)\pm \varepsilon}\, M.
$$
Then,
$$
\rho(M_\pm) = \frac{\rho(M)}{\rho(M)\pm \varepsilon},
$$
i.e.,
$$
\rho(M_+) < 1, \qquad \rho(M_-) > 1.
$$
In Step 3 we will show:
- $\exists\, k_+ \in \mathbb{N}\ \forall k\ge k_+:\ \|M_+^k\| < 1$
- $\exists\, k_- \in \mathbb{N}\ \forall k\ge k_-:\ \|M_-^k\| > 1$
Then, for
$$
k \ge \max\{k_+,k_-\},
$$
it follows that
$$
\|M^k\|^{1/k} = (\rho(M)\pm \varepsilon)\,\|M_\pm^k\|^{1/k},
$$
and hence
$$
\rho(M)-\varepsilon
\le
(\rho(M)-\varepsilon)\|M_-^k\|^{1/k}
=
\|M^k\|^{1/k}
=
(\rho(M)+\varepsilon)\|M_+^k\|^{1/k}
\le
\rho(M)+\varepsilon.
$$
This proves:
$$
\forall \varepsilon>0\ \exists k_0\in\mathbb{N}\ \forall k\ge k_0:
\quad
|\rho(M)-\|M^k\|^{1/k}| \le \varepsilon,
$$
and thus
$$
\rho(M)=\lim_{k\to\infty}\|M^k\|^{1/k}.
$$
---
**3)**
Let $B \in \{M_\pm\}$. 
Recall the Jordan normal form
![[Pasted image 20260319153954.png]]
$$
B = VJV^{-1},
$$
where $V \in \mathbb{C}^{n\times n}$ is regular, $J$ is block-diagonal,
$$
J =
\begin{pmatrix}
J_1 & &0 \\& \ddots \\
0 & &J_s
\end{pmatrix},
$$
with
$$
J_i =
\begin{pmatrix}
\lambda_i & 1 & 0 \\
& \ddots & \ddots \\
0 && \lambda_i
\end{pmatrix}
=
\lambda_i I_i + N_i \in \mathbb{R}^{r_i\times r_i}.
$$
🦭.
In particular,
$$
\sigma(B)=\{\lambda_1,\dots,\lambda_s\},
\qquad
N_i^{r_i}=0.
$$
(Thats a good guy :))
Clearly,
$$
B^k = VJ^kV^{-1}
$$
and
$$
J^k =
\begin{pmatrix}
J_1^k & & 0 \\
& \ddots & \\

0 & &J_s^k
\end{pmatrix},
$$
since $J$ is block-diagonal. (Anm.: JNF ist unstetig. ganz mies aus numerischer Sicht).

Recall that $\|\cdot\|_\infty$ induces the row-sum norm. (=good norm)
Hence,
$$
\|J^k\|_\infty = \max_{i=1,\dots,s}\|J_i^k\|_\infty.
$$
Recall the binomial formula: (=ugly guy :( )
$$
J_i^k = (\lambda_i I_i + N_i)^k
=
\sum_{j=0}^k \binom{k}{j}\lambda_i^{k-j}N_i^j
=
\sum_{j=0}^{r_i-1}\binom{k}{j}\lambda_i^{k-j}N_i^j,
=\lambda_{i}^k\sum_{j=0}^{r_{i}-1}\binom{k}{j}\lambda_{i}^{-j}N_{i}^j
$$
since $N_i^{r_i}=0$. O.B.d.A $\lambda_{i}\neq 0$ (for $k>r_{i}$) so this is a finite sum with polynomial growth in $k$.
If $|\lambda_i|>1$, then
$$
\|J_i^k\|_\infty \to \infty.
$$
If $|\lambda_i|<1$, then
$$
\|J_i^k\|_\infty \to 0,
$$
since $k^\alpha q^k$ is summable.
This yields
- $\|J^k\|_\infty \to \infty$ if  $\max_i |\lambda_i| = \rho(B) > 1$,
- $\|J^k\|_\infty \to 0$ if  $\max_i |\lambda_i| = \rho(B) < 1$.
Therefore (soft harvesting juhu)
$$
\|B^k\|_\infty
=
\|VJ^kV^{-1}\|_\infty
\le
\|V\|_\infty \|J^k\|_\infty \|V^{-1}\|_\infty
\to 0
\qquad \text{if } \rho(B)<1.
$$
Similarly,
$$
\|J^k\|_\infty
=
\|V^{-1}B^kV\|_\infty
\le
\|V^{-1}\|_\infty \|B^k\|_\infty \|V\|_\infty,
$$
which yields that
$$
\|B^k\|_\infty \to \infty
\qquad \text{if } \rho(B)>1.
$$
---
**4)**
From step 2 + 3, we infer
- $\|M_+^k\|_\infty \to 0$, since $\rho(M_+)<1$,
- $\|M_-^k\|_\infty \to \infty$, since $\rho(M_-) > 1$.

Since all norms on the finite-dimensional space $\mathbb{K}^{n\times n}$ are equivalent, we infer for the norm $\|\cdot\|$ on $\mathbb{K}^n$ and the induced matrix norm:
- $\|M_+^k\| \to 0$
- $\|M_-^k\| \to \infty$