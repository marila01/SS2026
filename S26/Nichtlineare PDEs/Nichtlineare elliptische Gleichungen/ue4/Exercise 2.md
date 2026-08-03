**(a):**
Prove that, if $H$ is a Hilbert space, then also $L^2(0,T;H)$ is a Hilbert space.

*Proof:*
Consider the $L^2(0,T;H)-$scalarproduct defined by
$$
\langle u,v \rangle_{L^2(0,T;H)}:=\langle u,v \rangle=\int_{0}^T (u(t),v(t))_{H}dt.
$$
Technically, we'd have to prove that this is bilinear, symmetric and positive definite, but this immediately follows from linearity of the integral and the bilinearity/symmetry/positive definiteness of the $H$-scalarproduct.

It remains to show that this space is complete w.r.t the induced norm.
We already know this kind of proof from measure theory.
Let $(u_{m})_{m}$ be a Cauchy-sequence in $L^2(0,T;H)$.
Because this is a Cauchy-sequence, there exists a subsequence $(u_{m_{_{j}}})_{j}$ such that
$$
||u_{m_{j+1}}-u_{m_{j}}||_{L^2}\leq \frac{1}{2^j}
$$
It holds that
$$
\begin{align}
\int_{0}^T||u_{m_{j+1}}(t)-u_{m_{j}}(t)||_{H}dt &\stackrel{C.S.}{\leq} \sqrt{ \int_{0}^T 1^2dt}\cdot \sqrt{ \int_{0}^T ||u_{m_{j+1}}(t)-u_{m_{j}}(t)||^2_{H}dt} \\
&=\sqrt{ T }||u_{m_{j+1}}-u_{m_{j}}||_{L^2} \\
&\leq \sqrt{ T } \frac{1}{2^j}
\end{align}
$$
This implies, that
$$
\sum_{j=0}^\infty \int_{0}^T||u_{m_{j+1}}(t)-u_{m_{j}}(t)||_{H}dt \text{ converges}.
$$
We can switch the integral and the sum (because monotone convergence) and get
$$
\int_{0}^T(\sum_{j=0}^\infty ||u_{m_{j+1}}(t)-u_{m_{j}}(t)||_{H})dt<\infty
$$
implying, that for almost every $t \in(0,T)$
$$
\sum_{j=0}^\infty||u_{m_{j+1}}(t)-u_{m_{j}}(t)||_{H}<\infty
$$
For those $t \in(0,T)$ and $k\geq j$ , it holds that
$$
||u_{m_{k}}(t)-u_{m_{j}}(t)||_{H}\leq \sum_{i=j}^{k-1}||u_{m_{i+1}}(t)-u_{m_{i}}(t)||_{H}\stackrel{k,j \to \infty}{\to}0
$$
So $(u_{m_{j}}(t))_{j}$ is a Cauchy-sequence for almost every $t \in(0,T)$.
Let $u(t):=\lim_{ j \to \infty }u_{m_{j}}(t)$.
We know, that $u$ is in $L^2(0,T;H)$, because of Fatou (and  its measurable as a pointwise limit of measurable functions):
$$
\int_{0}^T ||u(t)||^2dt=\int_{0}^T\lim\inf_{ j \to \infty }||u_{m_{j}}(t)||^2dt \leq \lim\inf_{ j \to \infty }\int_{0}^T||u_{m_{j}}(t)||^2dt < \infty
$$
because $u_{m_{j}}$ is Cauchy in $L^2(0,T;H)$.
Also
$$
||u_{m_{j}}(t)-u(t)||^2_{H}=\lim\inf_{ k \to \infty } ||u_{m_{j}}(t)-u_{m_{k}}(t)||_{H}^2
$$
Using Fatou again, we get $u_{m_{j}}\to u$ in $L^2(0,T;H)$.
$$
\begin{align}
||u_{m_{j}}-u||^2_{L^2}&=\int_{0}^T||u_{m_{j}}(t)-u(t)||^2_{H}dt \\
&= \int_{0}^T \lim\inf_{ k \to \infty }||u_{m_{j}}(t)-u_{m_{k}}(t)||^2_{H}dt  \\
&\leq \lim\inf_{ k \to \infty } \int_{0}^T||u_{m_{j}}(t)-u_{m_{k}}(t)||_{H}^2dt \\
&\leq \sup_{k\geq j}||u_{m_{j}}-u_{m_{k}}||^2_{L^2}
\end{align}
$$
$(u_{m})_{m}$ is Cauchy in $L^2(0,T;H)$, so we get $\lim_{ j \to \infty }\sup_{k\geq j}||u_{{m_{j}}}-u_{m_{k}}||^2_{L^2}=0$.
So $||u_{m_{j}}-u||_{L^2}\to 0$.
Because $(u_{m})_{m}$ is Cauchy in $L^2(0,T;H)$, we obtain
$$
u_{m}\to u \text{ in } L^2(0,T;H).
$$

**(b):**
Prove that $L^\infty(0,T;L^\infty(\Omega))$ does not coincide with $L^\infty((0,T)\times \Omega)$.

*Proof:*
Let $\Omega=(0,1)$.
Define $f:(0,1)\times(0,1)\to \mathbb{R}$,
$$
f(t,x):=\mathbb{1}_{\{ x<t \}}
$$
This is measurable on the product space, since
$$
\{ (t,x)\in(0,1)^2:x<t \} \subset(0,1)^2
$$
is open.
Also, $f$ is uniformly bounded, because $|f(t,x)|\leq 1$ for all $(t,x)$.
So $f \in L^\infty((0,1)\times(0,1))$.
Consider
$$
F:(0,1)\to L^\infty(0,1), F(t):=f(t,.)=\mathbb{1}_{(0,t)}
$$
which is the associated mapping to $f$.
Clearly this is bounded, so we need to show that this function isn't measurable.

Suppose it were measurable.
Then, there would be a sequence of step functions
$$
F_{n}(t)=\sum_{i=1}^{N_{n}}\mathbb{1}_{E_{n,i}}(t)x_{n,i}
$$
with $\bigcup_{i=1}^{N_{n}}E_{n,i}=(0,1)$, $E_{n,i}$ measurable and $F_{n}(t)\to F(t)$ almost everywhere, because this is a Banachspace.
Consider 
$$
D:=\{ x_{n,i}:n \in \mathbb{N},i=1,\dots,N_{n} \}
$$
which is countable.
Let
$$
X_{0}:=\overline{\text{span}_{\mathbb{Q}}D}.
$$
Then $X_{0}$ is separable, because $\text{span}_{\mathbb{Q}}D$ is countable and dense.
Also, for almost every $t \in(0,T)$, it holds that 
$$
F_{n}(t)\in X_{0}
$$
for every $n \in \mathbb{N}$.
Because $X_{0}$ is closed, $F(t) \in X_{0}$ for almost every $t$.
Let $N$ be this set of measure $0$.

On the other hand, for $s\neq t$, it holds that
$$
||F(t)-F(s)||_{L^\infty}=||\mathbb{1}_{(\min\{ s,t \},\max\{ s,t \})}||_{L^\infty}=1
$$
In particular, $F(t)\neq F(s)$ in $L^\infty(0,1)$.
Because $(0,1)\setminus N$ is uncountable, and $F$ injective, we have that
$$
\{ F(t):t\in(0,1)\setminus N \} \subset X_{0}
$$
is uncountable.
Because $X_{0}$ is separable, we can find a countable dense subset
$$
\{ x_{n}:n \in \mathbb{N} \} \subset X_{0}
$$

For every Point $F(t)$, consider $U_{\frac{1}{4}}(F(t))$.

Because those $F(t)$-points have distance $1$, every ball contains exactly one $F(t)$-value and the balls are disjoint.
Every ball must contain at least one $x_{n}$.
Because the Balls are disjoint, there can be at most countably many.
So $\{ F(t): t \in(0,1)\setminus N \}$ must be countable, which goes against our assumption.
So $F$ can't be measurable.