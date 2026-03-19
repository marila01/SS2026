Let $\Pi \in \mathbb{K}^{n \times n}$ with $\rho(\Pi) < 1$.
Then, $I-\Pi$ is regular and
$$

(I-\Pi)^{-1} = \sum_{k=0}^\infty \Pi^k.

$$
##### Proof:
Since $\rho(\Pi)<1$, we choose a norm on $\mathbb{C}^n$ such that $\|\Pi\|<1$.
Note that
$$

\left\|

\sum_{k=i}^{j}\Pi^k

\right\|

\le

\sum_{k=i}^{j}\|\Pi\|^k

\le

\|\Pi\|^i \frac{1}{1-\|\Pi\|}

\to 0

\qquad \text{as } i,j\to\infty.

$$
Hence, $\sum_{k=0}^{j}\Pi^k$ is a Cauchy sequence and its limit $\sum_{k=0}^\infty \Pi^k$ exists.
Note that
$$

(I-\Pi)\sum_{k=0}^\infty \Pi^k

=

\sum_{k=0}^\infty \Pi^k - \sum_{k=1}^\infty \Pi^k

= I.

$$
Hence, $I-\Pi$ is regular and
$$

(I-\Pi)^{-1} = \sum_{k=0}^\infty \Pi^k.

$$

  