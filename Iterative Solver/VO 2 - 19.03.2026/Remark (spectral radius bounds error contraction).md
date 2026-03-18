## Remark

Let $\|\cdot\|$ be a norm on $\mathbb{K}^n$, $M \in \mathbb{K}^{n\times n}$ with $\rho(M) < 1$ and $b, x_0 \in \mathbb{K}^n$. Consider the asymptotic error contraction of
$$
x_{k+1} := \Phi(b,x_k) = Mx_k + b.
$$

$$
q := \limsup_{k\to\infty}
\left(
\frac{\|x^*-x_k\|}{\|x^*-x_0\|}
\right)^{1/k}
=
\limsup_k
\left(
\frac{\|M^k(x^*-x_0)\|}{\|x^*-x_0\|}
\right)^{1/k}
$$
and thus
$$
\le \limsup_k \|M^k\|^{1/k} = \rho(M),
$$
by Gelfand's theorem.

i.e., $\rho(M)$ gives quite sharp bound on $q$ error contraction.