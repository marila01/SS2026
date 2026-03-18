## Corollary

Let $A = A^H \in \mathbb{K}^{u\times u}$ be regular and Hermitian.

Suppose that $A$ is positive definite, i.e.,
$$
(Ax,x)_2 > 0
\qquad
\forall x \in \mathbb{K}^n \setminus \{0\}.
$$

Then, any
$$
0 < \lambda < \frac{2}{\rho(A)}
$$
guarantees convergence of the damped Richardson iteration in the sense of
$$
\rho(I-\lambda A) < 1.
$$

In particular,
$$
\rho(A) < 2
$$
even yields convergence of the (undamped) Richardson iteration, i.e.,
$$
\rho(I-A) < 1.
$$

##### Proof

Note that
$$
\sigma(A) \subset \mathbb{R}_{>0}.
$$

We argue as before with
$$
|\widetilde u_{jj}| = |1-\lambda u_{jj}|.
$$

If
$$
\lambda u_{jj} \le 1,
$$
then
$$
|\widetilde u_{jj}| = |1-\lambda u_{jj}| = 1-\lambda u_{jj} < 1.
$$

If
$$
\lambda u_{jj} > 1,
$$
then
$$
|\widetilde u_{jj}| = \lambda u_{jj}-1 \le \lambda \rho(A)-1 < 1.
$$
