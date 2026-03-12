---
aliases:
  - "Lemma: Induced Matrix Norm"
---
# Lemma: Induced Matrix Norm

If $\lVert\cdot\rVert$ is a norm on $\mathbb{K}^{n}$, then the induced matrix norm is indeed a norm on $\mathbb{K}^{n\times n}$.

For $A,B \in \mathbb{K}^{n\times n}$ and $x \in \mathbb{K}^{n}$, there hold

$$
\lVert Ax\rVert \le \lVert A\rVert\,\lVert x\rVert
$$

and

$$
\lVert AB\rVert \le \lVert A\rVert\,\lVert B\rVert.
$$

Moreover, for any $\varepsilon > 0$, there exists $x_\varepsilon \in \mathbb{K}^{n}$ with $\lVert x_\varepsilon\rVert = \varepsilon$ such that

$$
\lVert A\rVert = \frac{\lVert A x_\varepsilon\rVert}{\lVert x_\varepsilon\rVert}.
$$
##### Proof:

Let $A,B \in \mathbb{K}^{n\times n}$, $\lambda \in \mathbb{K}$.

- If $\lVert A\rVert = 0$, then $Ax = 0$ for all $x \in \mathbb{K}^{n}$. Hence, $A = 0$.
- Since $\lVert \lambda A x\rVert = |\lambda|\,\lVert Ax\rVert$ for all $x \in \mathbb{K}^{n}$, it follows that
  $$
  \lVert \lambda A\rVert = |\lambda|\,\lVert A\rVert.
  $$
- Since $\lVert (A+B)x\rVert \le \lVert Ax\rVert + \lVert Bx\rVert$ for all $x \in \mathbb{K}^{n}$, it follows that
  $$
  \lVert A+B\rVert \le \lVert A\rVert + \lVert B\rVert.
  $$

Hence, the matrix norm is a norm on $\mathbb{K}^{n\times n}$.

- For $x \ne 0$, it holds
  $$
  \lVert Ax\rVert = \frac{\lVert Ax\rVert}{\lVert x\rVert}\,\lVert x\rVert \le \lVert A\rVert\,\lVert x\rVert.
  $$
  Since this holds trivially for $x=0$ (with equality), we are led to
  $$
  \lVert Ax\rVert \le \lVert A\rVert\,\lVert x\rVert.
  $$
- This also proves
  $$
  \lVert ABx\rVert \le \lVert A\rVert\,\lVert Bx\rVert \le \lVert A\rVert\,\lVert B\rVert\,\lVert x\rVert
  $$
  and hence
  $$
  \lVert AB\rVert \le \lVert A\rVert\,\lVert B\rVert.
  $$

It remains to prove that the supremum is indeed a maximum.

Define the sphere

$$
S := \{x \in \mathbb{K}^{n} \mid \lVert x\rVert = 1\}.
$$

Note that $S$ is bounded and closed (as the preimage of the closed set $\{1\}$). Hence, $S$ is compact and $\lVert A(\cdot)\rVert$ is continuous, since

$$
\bigl|\lVert Ax\rVert - \lVert Ay\rVert\bigr| \le \lVert Ax-Ay\rVert \le \lVert A\rVert\,\lVert x-y\rVert.
$$

Therefore, there exists $x_1 \in \mathbb{K}^{n}$ with $\lVert x_1\rVert = 1$ such that

$$
\lVert Ax_1\rVert = \max_{x \in S} \lVert Ax\rVert \le \lVert A\rVert = \sup_{x \in \mathbb{K}^{n}\setminus\{0\}} \frac{\lVert Ax\rVert}{\lVert x\rVert} \le \lVert Ax_1\rVert,
$$

because for any $x \ne 0$ one has $x/\lVert x\rVert \in S$ and

$$
\frac{\lVert Ax\rVert}{\lVert x\rVert} = \left\lVert A\left(\frac{x}{\lVert x\rVert}\right)\right\rVert.
$$

For any $\varepsilon > 0$, we may thus consider

$$
x_\varepsilon := \varepsilon x_1,
$$

since $\lVert x_\varepsilon\rVert = \varepsilon$ and

$$
\frac{\lVert A x_\varepsilon\rVert}{\lVert x_\varepsilon\rVert} = \lVert Ax_1\rVert.
$$
