---
aliases:
  - "Lemma: Relative Error Estimate"
---
# Lemma: Relative Error Estimate

Let $A \in \mathbb{K}^{n\times n}$ be regular. Let $x, \tilde{x}, b, \tilde{b} \in \mathbb{K}^n$ with $b \ne 0$ as well as

$$
Ax = b, \qquad A\tilde{x} = \tilde{b}.
$$

Then, it holds that

$$
\frac{\lVert x-\tilde{x}\rVert}{\lVert x\rVert}
\le
\operatorname{cond}_{\lVert\cdot\rVert}(A)
\frac{\lVert b-\tilde{b}\rVert}{\lVert b\rVert}.
$$

Moreover, this estimate is **sharp**: there exists $b \in \mathbb{K}^n\setminus\{0\}$ such that for all $\varepsilon>0$, there exists $\tilde{b} \in \mathbb{K}^n$ with $\lVert b-\tilde{b}\rVert \le \varepsilon$ such that the estimate holds with equality.

##### Proof:
Note that

$$
  \lVert x-\tilde{x}\rVert = \lVert A^{-1}(b-\tilde{b})\rVert \le \lVert A^{-1}\rVert\,\lVert b-\tilde{b}\rVert
  $$
$$
  \lVert b\rVert = \lVert Ax\rVert \le \lVert A\rVert\,\lVert x\rVert.
  $$

Combining this, we prove

$$
\frac{\lVert x-\tilde{x}\rVert}{\lVert x\rVert}
\le
\lVert A\rVert\,\lVert A^{-1}\rVert
\frac{\lVert b-\tilde{b}\rVert}{\lVert b\rVert}
=
\operatorname{cond}_{\lVert\cdot\rVert}(A)
\frac{\lVert b-\tilde{b}\rVert}{\lVert b\rVert}.
$$

To see that the estimate is sharp, we argue as follows:

- Choose $x \in \mathbb{K}^n\setminus\{0\}$ and $b := Ax$ such that
  $$
  \lVert A\rVert = \frac{\lVert Ax\rVert}{\lVert x\rVert} = \frac{\lVert b\rVert}{\lVert x\rVert}.
  $$
- For $\varepsilon > 0$, choose $y_\varepsilon \in \mathbb{K}^n\setminus\{0\}$ with $\lVert y_\varepsilon\rVert = \varepsilon$ such that
  $$
  \lVert A^{-1}\rVert = \frac{\lVert A^{-1} y_\varepsilon\rVert}{\lVert y_\varepsilon\rVert}.
  $$
- Choose
  $$
  \tilde{b} := b-y_\varepsilon
  \qquad\text{and}\qquad
  \tilde{x} := A^{-1}\tilde{b}.
  $$

This leads to

$$
x-\tilde{x} = A^{-1}(b-\tilde{b}) = A^{-1}y_\varepsilon
$$

and hence

$$
\frac{\lVert x-\tilde{x}\rVert}{\lVert x\rVert}
=
\frac{\lVert A^{-1}y_\varepsilon\rVert}{\lVert x\rVert}
=
\frac{\lVert A^{-1}y_\varepsilon\rVert}{\lVert y_\varepsilon\rVert}
\cdot
\frac{\lVert y_\varepsilon\rVert}{\lVert b\rVert}
\cdot
\frac{\lVert b\rVert}{\lVert x\rVert}
=
\lVert A^{-1}\rVert
\frac{\lVert b-\tilde{b}\rVert}{\lVert b\rVert}
\lVert A\rVert.
$$

Thus,

$$
\frac{\lVert x-\tilde{x}\rVert}{\lVert x\rVert}
=
\lVert A^{-1}\rVert\,\lVert A\rVert
\frac{\lVert b-\tilde{b}\rVert}{\lVert b\rVert}
=
\operatorname{cond}_{\lVert\cdot\rVert}(A)
\frac{\lVert b-\tilde{b}\rVert}{\lVert b\rVert},
$$

and $\lVert b-\tilde{b}\rVert = \lVert y_\varepsilon\rVert = \varepsilon$.
