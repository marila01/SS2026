---
aliases:
  - "Lemma: Characterizing the Spectral Radius"
  - "Lemma: Characterizing the Spectral Radius"
  - "Lemma: Characterizing the Spectral Radius"
---
# Lemma: Characterizing the Spectral Radius

Let $A \in \mathbb{K}^{n\times n}$.

Then,

$$
\rho(A) = \inf\left\{\lVert A\rVert \mid \lVert\cdot\rVert \text{ is matrix norm induced by norm on } \mathbb{K}^n\right\}.
$$

If $\sigma(A) \subseteq \mathbb{K}$, then norms on $\mathbb{K}^n$ (instead of $\mathbb{C}^n$) suffice.

##### Proof:
###### $\leq$:
Let $\lVert\cdot\rVert$ be a norm on $\mathbb{C}^n$. Let $d \in \sigma(A)$ and $x \in \mathbb{C}^n\setminus\{0\}$ with

$$
Ax = dx.
$$

Then,

$$
|d|\,\lVert x\rVert = \lVert dx\rVert = \lVert Ax\rVert \le \lVert A\rVert\,\lVert x\rVert.
$$

Hence,

$$
|d| \le \lVert A\rVert.
$$

If $\sigma(A) \subseteq \mathbb{K}$, then we can choose $x \in \mathbb{K}^n\setminus\{0\}$ and the same proof applies. Therefore, norms on $\mathbb{K}^n$ suffice in this case.
###### $\geq:$
According to linear algebra, $A$ is triangularizable:

$$
U := T^{-1}AT =
\begin{pmatrix}
U_{11} & \cdots & U_{1n} \\
 & \ddots & \vdots \\
0 & & U_{nn}
\end{pmatrix}
$$

with $T \in \mathbb{C}^{n\times n}$ regular and $U \in \mathbb{C}^{n\times n}$.

Note that

$$
\rho(A) = \max_{j=1,\dots,n} |U_{jj}|,
$$

since $\sigma(A) = \sigma(U) = \{U_{11},\dots,U_{nn}\}$.

Let $\varepsilon > 0$. We show that there exists a norm $\lVert\cdot\rVert_\varepsilon$ on $\mathbb{C}^n$ with

$$
\lVert A\rVert_\varepsilon \le \rho(A) + C\varepsilon
$$

for some fixed $C > 0$.

Let

$$
D_\varepsilon := \operatorname{diag}(1,\varepsilon,\dots,\varepsilon^{n-1}).
$$

Define

$$
\lVert x\rVert_\varepsilon := \lVert D_\varepsilon^{-1}T^{-1}x\rVert_\infty.
$$

Note that

$$
\lVert A\rVert_\varepsilon
=
\sup_{x \in \mathbb{C}^n\setminus\{0\}} \frac{\lVert Ax\rVert_\varepsilon}{\lVert x\rVert_\varepsilon}
=
\sup_{x \in \mathbb{C}^n\setminus\{0\}} \frac{\lVert D_\varepsilon^{-1}T^{-1}Ax\rVert_\infty}{\lVert D_\varepsilon^{-1}T^{-1}x\rVert_\infty}.
$$

With the substitution

$$
y = D_\varepsilon^{-1}T^{-1}x
\qquad\text{or equivalently}\qquad
x = TD_\varepsilon y,
$$

this becomes

$$
\lVert A\rVert_\varepsilon = \sup_{y \in \mathbb{C}^n\setminus\{0\}} \frac{\lVert D_\varepsilon^{-1}T^{-1}ATD_\varepsilon y\rVert_\infty}{\lVert y\rVert_\infty} = \lVert D_\varepsilon^{-1} U D_\varepsilon\rVert_\infty.
$$

Note that

- multiplication with diagonal matrix from the left = scaling of rows,
- multiplication with diagonal matrix from the right = scaling of columns.

Hence,

$$
D_\varepsilon^{-1}UD_\varepsilon =
\begin{pmatrix}
U_{11} & \varepsilon U_{12} & \cdots & \varepsilon^{n-1}U_{1n} \\
 & U_{22} & \cdots & \varepsilon^{n-2}U_{2n} \\
 & & \ddots & \vdots \\
0 & & & U_{nn}
\end{pmatrix}.
$$

Recall that

$$
\lVert A\rVert_\infty = \max_j \sum_k |A_{jk}|
$$

is the so-called row-sum norm.

Hence,

$$
\lVert A\rVert_\varepsilon = \lVert D_\varepsilon^{-1} U D_\varepsilon\rVert_\infty = \max_j \left(|U_{jj}| + \sum_{k=j+1}^n \varepsilon^{k-j}|U_{jk}|\right)
$$

and therefore

$$
\lVert A\rVert_\varepsilon
\le
\max_j |U_{jj}| + \max_j \sum_{k=j+1}^n \varepsilon^{k-j}|U_{jk}|
\le
\rho(A) + \varepsilon \sum_{j<k} |U_{jk}|
\le
\rho(A) + C\varepsilon.
$$

Note that the estimate "$\ge$" is independent of $\sigma(A) \subseteq \mathbb{K}$, since $\lVert\cdot\rVert_\varepsilon$ is of course a norm on $\mathbb{K}^n$ if it is a norm on $\mathbb{C}^n$.