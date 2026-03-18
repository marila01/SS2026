## Remark

Convergence of a basic linear iteration can be slow and non-monotonically.

For instance,
$$
M :=
\begin{pmatrix}
0 & * \\
& \ddots \\
&& 0
\end{pmatrix}
\in \mathbb{R}^{n\times n}
$$
satisfies
$$
\rho(M)=0, \qquad M^u=0,
$$
but
$$
\|M\|_1 = \|M\|_2 = \|M\|_\infty = u.
$$

One observes essentially no convergence for \( k \le u \) and
$$
x^* = \sum_{j=0}^{u-1} M^j b.
$$
