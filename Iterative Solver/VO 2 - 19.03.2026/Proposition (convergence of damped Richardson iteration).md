## Proposition (convergence of damped Richardson iteration)

Let $A \in \mathbb{K}^{n\times n}$ regular with
$$
\operatorname{Re}(\mu) > 0
\qquad \text{for all } \mu \in \sigma(A).
$$

Then, there exists $\lambda_{0} > 0$ such that $\forall \lambda \in(0,\lambda_{0})$:
$$
\rho(I-\lambda A) < 1.
$$
In this case, the damped Richardson iteration leads to convergence for any $b \in \mathbb{K}^n$ and any initial guess $x_0 \in \mathbb{K}^n$. The limit
$$
x^* = \lim_{k\to\infty} x_k,
\qquad
x_{k+1} := \Phi(b,x_k)
$$
solves
$$
Ax^* = b.
$$
##### Proof
Recall that $A$ is triangularizable, i.e., there exist $T \in \mathbb{C}^{n\times n}$ regular and $U \in \mathbb{C}^{n\times n}$ upper triangular with
$$
A = T^{-1}UT.
$$
In particular,
$$
\sigma(A) = \{u_{jj} \mid j=1,\dots,u\}.
$$
Moreover,
$$
I-\lambda A = T^{-1}(I-\lambda U)T
$$
with $\widetilde U:=I-\lambda U$ upper triangular.
In particular,
$$
\sigma(I-\lambda A) = \{\widetilde u_{jj} \mid j=1,\dots,u\}.
$$
This yields
$$
|\widetilde u_{jj}|^2
=
|1-\lambda \operatorname{Re}u_{jj}|^2 + |\lambda \operatorname{Im}u_{jj}|^2
$$
and hence
$$
=
1 - 2\lambda \operatorname{Re}u_{jj}
+ \lambda^2 |\operatorname{Re}u_{jj}|^2
+ \lambda^2 |\operatorname{Im}u_{jj}|^2
$$
so
$$
=
1 - \lambda\bigl(2\operatorname{Re}u_{jj} - \lambda |u_{jj}|^2\bigr) < 1
$$
for $\lambda$ sufficiently small.
Since
$$
\rho(I-\lambda A) = \max_j |\widetilde u_{jj}|,
$$
there exists $\lambda_0 > 0$ such that
$$
\rho(I-\lambda A) < 1
\qquad \text{for all } 0 < \lambda \le \lambda_0.
$$
The rest of the claims follow from the convergence theorem.