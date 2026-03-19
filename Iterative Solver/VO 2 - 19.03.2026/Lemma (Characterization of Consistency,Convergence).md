---
aliases:
  - Lemma (Characterization of Consistency/Convergence)
---
Let $\Pi, N \in \mathbb{K}^{n \times n}$, let $A \in \mathbb{K}^{n \times n}$ regular, let

$$

\Phi(b,x) := \Pi x + Nb.

$$
Then, there holds the following:
1. If $\Phi$ is consistent, then $I-\Pi$ is regular if and only if $N$ is regular.
2. If $\Phi$ is convergent, then $I-\Pi$ is regular.
3. If $\Phi$ is consistent and convergent, then $I-\Pi$ and $N$ are regular.

##### Proof:
1. For all $x \in \mathbb{K}^n$ holds
   $$

   x = \Phi(Ax, x) = \Pi x + NAx.

   $$

   Hence,
   $$

   I = \Pi + NA

   $$
   or equivalently
   $$

   I-\Pi = NA.

   $$
   Since $A$ is regular, it follows that
   $$

   I-\Pi \text{ regular } \Longleftrightarrow N \text{ regular.}

   $$
2. If $I-\Pi$ is **not** regular, then there exists $x \in \mathbb{K}^n \setminus \{0\}$ with
   $$

   (I-\Pi)x = 0.

   $$
   Hence,
   $$

   \Pi x = x,

   $$
   i.e., $x$ is an eigenvector and $1 \in \sigma(\Pi)$.
   In particular, it follows
   $$

   \rho(\Pi) \ge 1.

   $$

   However, convergence of a linear iteration yields $\rho(\Pi) < 1$.
   Therefore, $I-\Pi$ must be regular.
   
3. According to (ii), $I-\Pi$ is regular (by convergence).
   According to (i), this gives regularity of $N$ (by consistency).