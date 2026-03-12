---
aliases:
  - "Theorem: Global Convergence of Basic Iterative Methods"
  - "Theorem: Global Convergence of Basic Iterative Methods"
---
## Theorem: Global convergence of basic iterative methods

For any matrix $A \in \mathbb{K}^{n\times n}$, the following is equivalent:

1. $$
   \rho(A) < 1
   $$
2. There exist $b \in \mathbb{K}^{n}$ and $x_0 \in \mathbb{K}^{n}$ such that
   $$
   \Phi(x) := Ax + b
   $$
   and
   $$
   x_{k+1} := \Phi(x_k) \qquad \text{for all } k \in \mathbb{N}_0
   $$
   guarantees convergence, i.e.,
   $$
   x^* := \lim_{k\to\infty} x_k
   $$
   exists.
3. For all $b \in \mathbb{K}^{n}$ and all $x_0 \in \mathbb{K}^{n}$, the definition
   $$
   \Phi(x) := Ax + b
   $$
   and
   $$
   x_{k+1} := \Phi(x_k) \qquad \text{for all } k \in \mathbb{N}_0
   $$
   guarantees convergence.

In this case, $x^*$ is uniquely determined by $b$, and there exists a norm $\lVert\cdot\rVert$ on $\mathbb{K}^{n}$ such that

$$
\lVert \Phi(x)-\Phi(y)\rVert \le q\,\lVert x-y\rVert
\qquad \forall x,y \in \mathbb{K}^{n}
$$

and $0<q<1$.

##### Proof:
The implication $(iii) \Rightarrow (ii)$ is obvious.

*$(i) \Rightarrow (iii)$:

According to the previous lemma, there exists a norm $\lVert\cdot\rVert$ on $\mathbb{C}^{n}$ with

$$
\lVert A\rVert < 1.
$$

For any $b \in \mathbb{K}^{n}$, this yields

$$
\lVert \Phi(x)-\Phi(y)\rVert = \lVert Ax-Ay\rVert \le \lVert A\rVert\,\lVert x-y\rVert.
$$

Hence, $\Phi$ satisfies the assumptions of the Banach fixed point theorem with

$$
q := \lVert A\rVert < 1.
$$

**$(ii) \Rightarrow (i)$ for $\mathbb{K} = \mathbb{C}$:

Let $\lVert\cdot\rVert$ be any norm on $\mathbb{C}^{n}$. Let $d \in \sigma(A)$ with

$$
|d| = \rho(A).
$$

Let $v \in \mathbb{C}^{n}\setminus\{0\}$ with

$$
Av = dv.
$$

Define

$$
x_0 := v + x^*
$$

and hence

$$
x_0 - x^* = v.
$$

Then,

$$
|d|^{k} \lVert x_0-x^*\rVert = |d|^{k} \lVert v\rVert = \lVert A^{k}(x_0-x^*)\rVert = \lVert x_k-x^*\rVert \to 0.
$$

Therefore,

$$
\rho(A) = |d| < 1.
$$

**NB:** $(ii)$ for $\mathbb{R}$ $\Rightarrow$ $(i)$ for $\mathbb{C}$.


