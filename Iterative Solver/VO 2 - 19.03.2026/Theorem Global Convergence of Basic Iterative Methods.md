## Theorem (global convergence of basic iterative methods)

Let $M \in \mathbb{K}^{n \times n}$. Define
$$
\Phi : \mathbb{K}^u \times \mathbb{K}^n \to \mathbb{K}^n, \qquad \Phi(b,x) := Mx + b.
$$

Then, the following is equivalent:

1. $\rho(M) < 1$

2. 
$$
\forall b \in \mathbb{K}^n \ \exists x^* \in \mathbb{K}^n \ \forall x_0 \in \mathbb{K}^n, \quad x_{k+1} := \Phi(b,x_k) : \quad x^* = \lim_{k\to\infty} x_k.
$$

In this case $x^* = \Phi(b,x^*)$ is uniquely determined by $(M,b)$, and there exists a norm $\|\cdot\|$ on $\mathbb{K}^n$ such that
$$
0 < q := \|M\| < 1
$$
and
$$
\|\Phi(b,x)-\Phi(b,y)\| \le q \|x-y\|
\qquad
\forall b \in \mathbb{K}^n \ \forall x,y \in \mathbb{K}^n.
$$

---

##### Proof $(i \Rightarrow ii)$

According to the previous lemma, there exists a norm $\|\cdot\|$ on  $\mathbb{C}^n$ (and hence on $\mathbb{K}^n$) with
$$
\|M\| = q < 1.
$$

For any  $b \in \mathbb{K}^n$, $x,y \in \mathbb{K}^n$, this yields
$$
\|\Phi(b,x)-\Phi(b,y)\|
=
\|Mx-My\|
\le
\|M\|\,\|x-y\|
=
q\|x-y\|.
$$

Hence,  $\Phi(b,\cdot) : \mathbb{K}^n \to \mathbb{K}^n$  satisfies Banach's fixed point theorem.

---

##### Proof $(ii \Rightarrow i)$ for  $\mathbb{K} = \mathbb{C}$

Let  $b \in \mathbb{C}^n$, choose $x^*$ accordingly.

Recall that limits of fixed point iterations are fixed points,
$$
x^* = \Phi(b,x^*).
$$

Let $\lambda \in \sigma(M)$ with $|\lambda| = \rho(M)$.

Let $v \in \mathbb{C}^n$ with $\|v\| = 1$ and $Mv = \lambda v$.

Choose
$$
x_0 := v + x^* \in \mathbb{C}^n.
$$

Note
$$
x^* - x_1
=
\Phi(b,x^*) - \Phi(b,x_0)
=
M(x^* - x_0)
=
\lambda \underbrace{\frac{x^* - x_0}{v}}_{=\,v}.
$$

Hence
$$
x^* - x_k = \lambda^k v
$$
by induction.

Therefore,
$$
\rho(M)^k
=
|\lambda|^k
=
\|\lambda^k v\|
=
\|x^* - x_k\|
\to 0
\qquad \text{by (ii).}
$$

Therefore,
$$
\rho(M) < 1.
$$

---

##### Proof of $(ii)$ for  $\mathbb{K} = \mathbb{R} \Rightarrow (ii)$ for $\mathbb{K} = \mathbb{C}$
Note that the previous argument cannot be applied to prove (i), since
$$
\lambda \notin \mathbb{R} \text{ in general.}
$$

Hence, we argue differently and suppose that (ii) holds for  $\mathbb{K} = \mathbb{R}$.

Note that
$$
\operatorname{Re}(Mx) = M(\operatorname{Re}x), \qquad \operatorname{Im}(Mx) = M(\operatorname{Im}x)
$$
for all $x \in \mathbb{C}^n$, since $M \in \mathbb{R}^{n\times n}$!

Let $b \in \mathbb{C}^n$.

Apply (ii) for $\operatorname{Re} b, \operatorname{Im} b \in \mathbb{R}^n$.

Obtain $x^* \in \mathbb{C}^n$ s.t. (ii) holds for $\operatorname{Re} b, \operatorname{Re} x^*$ and $\operatorname{Im} b, \operatorname{Im} x^*$.

Let $x_0 \in \mathbb{C}^n$,
$$
x_{k+1} := \Phi(b,x_k) = Mx_k + b.
$$

Then,
$$
\operatorname{Re} x_{k+1} = M(\operatorname{Re} x_k) + \operatorname{Re} b \to \operatorname{Re} x^*
$$
and
$$
\operatorname{Im} x_{k+1} = M(\operatorname{Im} x_k) + \operatorname{Im} b \to \operatorname{Im} x^*.
$$

Hence,
$$
x_{k+1} \to x^* \text{ in } \mathbb{C}^n,
$$
so that (ii) holds for $\mathbb{C}$.

Now, (i) follows.