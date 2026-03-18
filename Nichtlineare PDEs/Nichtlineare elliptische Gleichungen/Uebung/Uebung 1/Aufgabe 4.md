Prove the claim on Remark (i) on page 17 of the lecture notes:
If $|f(x,\lambda)-f(x,\eta)|\leq L_{0}|\lambda-\eta|$ for almost every $x \in \Omega$, $\lambda,\eta \in \mathbb{R}$ and $L_{0}$ is small enough, then the solution is unique.

##### Proof:
We want to use Banachs fixed point theorem ![[Theorem 2.2 - Fixpunktsatz von Banach]]
to show, that our problem has an unique solution.

We know, that $H^1(\Omega)$ is a Banach space.
Let $M:=\{ v \in H^1(\Omega) \quad | \quad v=g \text{ on } \partial \Omega \}$.
Then $M\subset H^1(\Omega)$ is closed.

For $v \in H^1(\Omega)$, let $u_{v}$ be the unique solution to
$$
\begin{cases}
L(u)=f(x,v(x)) \quad \text{ auf } \Omega, \\
u=g \text{ auf } \partial \Omega
\end{cases}
$$
Define $S:M\to M$ as $v\mapsto S(v):=u_{v}$.

This mapping is well defined, because of results from linear elliptic PDEs:

$f(.,v) \in H^{-1}(\Omega)$ for fixed $v$, because 
$$| f(x, v(x))| \leq h(x) \in L^q (Ω) \hookrightarrow H^{−1}(\Omega).$$

Also $S:M\to M$ per definitionem of the operator.

For $v_{1},v_{2}\in M$, $u_{v_{1}}-u_{v_{2}}$ solves
$$
\begin{cases}
L(u)=f(x,v_{1})-f(x,v_{2}) \text{ in } \Omega \\
u=0 \text{ on } \partial \Omega

\end{cases}
$$
It follows from the theory of linear elliptic PDEs, that
$$
||S(v_{1})-S(v_{2})||_{H^1(\Omega)}=||u_{v_{1}}-u_{v_{2}}||_{H^1(\Omega)}\leq C||f(.,v_{1})-f(.,v_{2})||_{H^{-1}(\Omega)}
$$
with $C=C(\alpha, c,\Omega)$.
Because 
$$
||f(.,v_{1})-f(.,v_{2})||_{H^{-1}(\Omega)}=\mathrm{sup}_{\varphi \in H_{0}^1(\Omega),||\varphi||_{H^1(\Omega)}\leq 1}
|\int_{\Omega}(f(x,v_{1}(x))-f(x,v_{2}(x)))\varphi(x)dx|\leq L_{0}||v_{1}-v_{2}||_{H^1(\Omega)},$$
we get $||S(v_{1})-S(v_{2})||_{H^1(\Omega)}\leq \underbrace{CL_{0}}_{=:k}||v_{1}-v_{2}||_{H^1(\Omega)}$
with $k=CL_{0}<1 \iff L_{0}< \frac{1}{C}$.
So we can apply [[Theorem 2.2 - Fixpunktsatz von Banach]] and get an unique solution.
![[Pasted image 20260317162711.png]]
![[Pasted image 20260317162957.png]]
