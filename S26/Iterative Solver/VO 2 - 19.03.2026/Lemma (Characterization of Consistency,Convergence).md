---
aliases:
  - Lemma (Characterization of Consistency/Convergence)
---
Let $M, N \in \mathbb{K}^{n \times n}$, let $A \in \mathbb{K}^{n \times n}$ regular, let

$$ \Phi(b,x) := M x + Nb.$$
Then, there holds the following:
1. If $\Phi$ is consistent, then $I-M$ is regular if and only if $N$ is regular.
2. If $\Phi$ is convergent, then $I-M$ is regular.
3. If $\Phi$ is consistent and convergent, then $I-M$ and $N$ are regular.

##### Proof:
1. For all $x \in \mathbb{K}^n$ holds $$x = \Phi(Ax, x) = M x + NAx.$$
   Hence,
$$I = M + NA$$
   or equivalently $$I-M = NA.$$
   Since $A$ is regular, it follows that
   $$I-M \text{ regular } \Longleftrightarrow N \text{ regular.}$$
2. If $I-M$ is **not** regular, then there exists $x \in \mathbb{K}^n \setminus \{0\}$ with
$$(I-M)x = 0.$$
	Hence,
$$M x = x,$$
   i.e., $x$ is an eigenvector and $1 \in \sigma(M)$.
   In particular, it follows
$$\rho(M) \ge 1.$$

   However, convergence of a linear iteration yields $\rho(M) < 1$.
   Therefore, $I-M$ must be regular.
   
3. According to (ii), $I-M$ is regular (by convergence).
   According to (i), this gives regularity of $N$ (by consistency).