Let $M \in \mathbb{K}^{n \times n}$ with $\rho(M) < 1$.
Then, $I-M$ is regular and
$$

(I-M)^{-1} = \sum_{k=0}^\infty M^k.

$$
##### Proof:
Since $\rho(M)<1$, we choose a norm on $\mathbb{C}^n$ such that $\|M\|<1$.
Note that
$$

\left\|

\sum_{k=i}^{j}M^k

\right\|

\le

\sum_{k=i}^{j}\|M\|^k

\le

\|M\|^i \frac{1}{1-\|M\|}

\to 0

\qquad \text{as } i,j\to\infty.

$$
Hence, $\sum_{k=0}^{j}M^k$ is a Cauchy sequence and its limit $\sum_{k=0}^\infty M^k$ exists.
Note that
$$

(I-M)\sum_{k=0}^\infty M^k

=

\sum_{k=0}^\infty M^k - \sum_{k=1}^\infty M^k

= I.

$$
Hence, $I-M$ is regular and
$$

(I-M)^{-1} = \sum_{k=0}^\infty M^k.

$$

  