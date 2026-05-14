Prove the lemma on page 56 of the lecture notes.
**Lemma:**
Let $z:[0,T]\to[0,+\infty)$ be $C ^1$, and let $u \in W^{1,2}(0,T;H^1_{0}(\Omega),L^2(\Omega))$.
Then, $\forall \tau \in[0,T]$, it holds
$$
\int_{0}^\tau \langle u_{t},(u-z)^+ \rangle_{H^{-1},H_{0}^1}dt=\frac{1}{2}\int_{\Omega}((u-z)^+(\tau)^2-(u-z)^+(0)^2)dx+\int_{0}^\tau \int_{\Omega}z_{t}(u-z)^+dxdt
$$
*Proof:*
Let $w(t,x):=(u(t,x)-z(t))^+$.
Since $u \in W^{1,2}(0,T;H_{0}^1(\Omega),L^2(\Omega))$, we have $u \in C([0,T];L^2(\Omega))$.
So $w(t)\in L^2(\Omega)$ is well-defined for every $t \in[0,T]$.
Since $u(t)\in H_{0}^1(\Omega)$ and $z(t)\geq 0$, we have $w(t)=(u(t)-z(t))^+ \in H_{0}^1(\Omega)$.

By Stampacchia (ignore that we're banach space valued ups), we get for almost every $t \in(0,T)$
$$
\partial_{t}(u-z)^+=\mathbb{1}_{u>z}(u-z)_{t}.
$$
We also know, that
$$
(u-z)^+=(u-z)\mathbb{1}_{u>z}.
$$
Consider $F(t):=\frac{1}{2}\int_{\Omega}[(u(t)-z(t))^+]^2dx$.
We've already proven the chainrule for Sobolev functions a few exercises ago, so we get
$$
\begin{align}
F'(t)&=\int_{\Omega}(u-z)^+ \partial_{t}(u-z)^+dx \\
&=\int_{\Omega}\mathbb{1}_{u>z}(u-z)^+(u-z)_{t}dx \\
&=\int_{\Omega}(u-z)^+(u-z)_{t}dx \\
&=\langle u_{t},(u-z)^+ \rangle_{H^{-1},H_{0}^1}-\int_{\Omega}z_{t}(u-z)^+dx
\end{align}
$$
for almost every $t \in(0,T)$.
This also shows that $F$ is absolutely continous, so integrating in $t$ yields
$$
F(\tau)-F(0)=\int_{0}^\tau \langle u_{t},(u-z)^+ \rangle_{H^{-1},H_{0}^1}dt- \int_{0}^\tau\int_{\Omega} z_{t}(u-z)^+dxdt
$$
which we had to show.
