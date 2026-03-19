## Example (damped Richardson iteration)

Let $A \in \mathbb{K}^{n\times n}$ regular, $b \in \mathbb{K}^n$.

We seek $x^* \in \mathbb{K}^n$ with
$$
Ax^* = b.
$$
Note that $\forall \lambda \in \mathbb{K}:$
$$
-\lambda A x^* + \lambda b = 0.
$$
Hence, consider
$$
\Phi(b,x) := (I-\lambda A)x + \lambda b
= x + \lambda(b-Ax)
$$
with
$$
M := I-\lambda A,
$$
and $b-Ax$ the so-called residual.

**KNOWN**: iteration converges if $\rho(M) < 1$.