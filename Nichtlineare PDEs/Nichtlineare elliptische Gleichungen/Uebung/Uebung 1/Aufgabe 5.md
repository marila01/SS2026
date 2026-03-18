Let $\Omega \subset \mathbb{R}^n$ be open, bounded with Lipschitz boundary. Prove that if $F \in C^1(\mathbb{R})$ with $F'\in L^\infty(\mathbb{R})$, and $u \in W^{1,p}(\Omega),1<p<+\infty$, then $F \circ u \in W^{1,p}(\Omega)$ and $F'(u)\nabla u=\nabla(F\circ u)$.
Where does the proof fail for unbounded $\Omega$? 
Can you adapt the assumptions on $F$ to make the proof work?
wo 
##### Proof:
Let $x \in \Omega$. Then (from the mean value theorem), we deduce
$$
|F(u(x))|^p=|F(u(x))-F(0)+F(0)|^p\leq C(||F'||_{\infty}^p|u(x)|^p+|F(0)|^p)
$$
which is integrable, because $\Omega$ is bounded and $u \in L^p(\Omega)$, so $F\circ u \in L^p(\Omega)$ and also $F \circ u \in L^1_{loc}(\Omega)$, because $\lambda(\Omega)<\infty$.

We also know, that $F'(u)\nabla u\in L^p(\Omega)\cap L^1_{loc}(\Omega)$, because
$\forall x \in \Omega: ||F'(u(x))\nabla u(x)<|^p=|F'(u(x))|^p||\nabla u(x)||^p\leq||F'||_{\infty}^p|\nabla u(x)|^p.$

We know that $\exists u_{n} \in C^\infty(\bar{\Omega})$ with $u_{n}\to u$ in $W^{1,p}(\Omega)$ because $C^\infty(\bar{\Omega})$ lies densely in $W^{1,p}(\Omega)$
It holds, that
$$
\nabla(F\circ u_{n})=F'(u_{n})\nabla u_{n}
$$
And, similarily to the argument in the beginning:
$$ ||F(u_{n})-F(u)||_{L^p(\Omega)}\leq ||F'||_{\infty} ||u_{n}-u||_{L^p(\Omega)}\to 0
$$
Now
$$
\begin{align}
||F'(u_{n})\nabla u_{n}-F'(u)\nabla u||_{L^p(\Omega)}&=||F'(u_{n})(\nabla u_{n}-\nabla u)+(F'(u_{n})-F'(u))\nabla u||_{L^p(\Omega)} \\
&\leq ||F'||_{\infty}||\nabla u_{n}-\nabla u||_{L^p(\Omega)}+||(F'(u_{n})-F'(u))\nabla u||_{L^p(\Omega)}
\end{align}
$$
The first term tends to $0$.

Since $F'$ is continous and $u_{n}\to u$ almost everywhere, it follows, that $F'(u_{n})\to F'(u)$ almost everywhere.
Also, $(|F'(u_{n})-F'(u)|||\nabla u||)^p\leq 2^p ||F'||_{\infty}^p||\nabla u||^p \in L^1(\Omega)$.

By dominated convergence, the second term tends to $0$ as $n \to \infty$.

That implies $F'(u_{n})\nabla u_{n}\to F'(u)\nabla u$ in $L^p(\Omega)$.

For for $\varphi \in C_{0}^\infty$, it holds, that
$$
\langle F'(u)\nabla u,\varphi\rangle\leftarrow \langle F'(u_{n})\nabla u_{n},\varphi\rangle=\langle \nabla(F\circ u_{n}),\varphi\rangle=-\langle F \circ u_{n},\nabla \varphi \rangle \to -\langle F \circ u,\nabla \varphi\rangle = \langle \nabla(F \circ u),\varphi\rangle.
$$
because of the $L^p(\Omega)$-convergencies above.

The proof uses the boundedness of $\Omega$ in the step, where we prove $F \circ u \in L^p(\Omega)$. We can fix that, by the assumption $F(0)=0$.

