
## Banach Fixed Point Theorem

Let $X$ be a Banach space, i.e., a complete normed space. Let $0<q<1$ and let $\Phi : X \to X$ satisfy

$$
\lVert \Phi(x)-\Phi(y)\rVert \le q\,\lVert x-y\rVert
\qquad \forall x,y \in X.
$$

Then, there exists a unique $x^* \in X$ such that

$$
\Phi(x^{*}) = x^{*}.
$$

Moreover, it holds that:

1. For each $x_0 \in X$ and
   $$
   x_{k+1} := \Phi(x_k) \qquad \text{for all } k \in \mathbb{N}_0,
   $$
   there holds
   $$
   \lVert x^{*}-x_k\rVert \to 0 \qquad \text{as } k \to \infty.
   $$
2. $$
   \lVert x^{*}-x_{k+1}\rVert \le q\,\lVert x^{*}-x_k\rVert
   $$
3. $$
   \lVert x^{*}-x_{k+1}\rVert \le \frac{q}{1-q}\,\lVert x_{k+1}-x_k\rVert \le \frac{q^{k+1}}{1-q}\,\lVert x_1-x_0\rVert
   $$
4. $$
   \lVert x_{k+1}-x_k\rVert \le (1+q)\,\lVert x^{*}-x_k\rVert
   $$
##### Proof:
**Step 1 (uniqueness)**

For $x^{*} = \Phi(x^{*})$ and $y^{*} = \Phi(y^{*})$, it holds that

$$
\lVert x^{*}-y^{*}\rVert = \lVert \Phi(x^{*})-\Phi(y^{*})\rVert \le q\,\lVert x^{*}-y^{*}\rVert.
$$

Hence, $x^{*} = y^{*}$ since $0<q<1$.

**Step 2 (the limit will be a fixed point)**

For $x_0 \in X$, consider

$$
x_{k+1} := \Phi(x_k).
$$

Suppose that the limit

$$
x^{*} := \lim_{k\to\infty} x_k
$$

exists. Then,

$$
x^{*} = \lim_{k\to\infty} x_k = \lim_{k\to\infty} x_{k+1} = \lim_{k\to\infty} \Phi(x_k) = \Phi\left(\lim_{k\to\infty} x_k\right) = \Phi(x^{*}),
$$

using continuity of $\Phi$.

**Step 3 ($(x_k)_{k\in\mathbb{N}}$ is a Cauchy sequence)**

For $m \le n$, it holds that

$$
\lVert x_n-x_m\rVert \le \sum_{k=m}^{n-1} \lVert x_{k+1}-x_k\rVert.
$$

Moreover,

$$
\lVert x_{k+1}-x_k\rVert = \lVert \Phi(x_k)-\Phi(x_{k-1})\rVert \le q\,\lVert x_k-x_{k-1}\rVert \le q^{k} \lVert x_1-x_0\rVert.
$$

Thus,

$$
\lVert x_n-x_m\rVert \le \lVert x_1-x_0\rVert \sum_{k=m}^{n-1} q^{k} \le \lVert x_1-x_0\rVert \frac{q^{m}}{1-q}.
$$

Now the right-hand side tends to zero as $m \to \infty$. Hence, $(x_k)$ is a Cauchy sequence.

Since $X$ is a Banach space, the limit

$$
x^{*} := \lim_{k\to\infty} x_k
$$

exists (and is a fixed point).

**Step 4 (error estimates)**

$$
\lVert x^{*}-x_{k+1}\rVert = \lVert \Phi(x^{*})-\Phi(x_k)\rVert \le q\,\lVert x^{*}-x_k\rVert.
$$

Hence,

$$
\lVert x^{*}-x_{k+1}\rVert \le \frac{q}{1-q}\,\lVert x_{k+1}-x_k\rVert,
$$

because

$$
\lVert x^{*}-x_k\rVert \le \lVert x^{*}-x_{k+1}\rVert + \lVert x_{k+1}-x_k\rVert.
$$

Also,

$$
\lVert x_{k+1}-x_k\rVert \le q^{k} \lVert x_1-x_0\rVert,
$$

and therefore

$$
\lVert x^*-x_{k+1}\rVert \le \frac{q^{k+1}}{1-q}\,\lVert x_1-x_0\rVert.
$$

And,

$$
\lVert x_{k+1}-x_k\rVert \le \lVert x^*-x_{k+1}\rVert + \lVert x^*-x_k\rVert \le (1+q)\,\lVert x^*-x_k\rVert.
$$
