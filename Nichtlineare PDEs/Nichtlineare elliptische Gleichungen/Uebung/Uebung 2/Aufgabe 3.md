Let $\Omega \subset \mathbb{R}^n$ be a bounded domain with smooth boundary. Consider
$$
\begin{cases}
- \Delta u = \lambda e^u \quad \text{ in } \Omega, \\
u = 0 \quad \text{ auf } \partial \Omega,
\end{cases}
$$
where $\lambda >0$ is a real parameter.
#### (a)
##### (i) Derive the weak formulation
Let $v \in H_{0}^1(\Omega)$.
We want $u \in H_{0}^1(\Omega)$ such that
$$
-\int_{\Omega}(\Delta u)vdx \stackrel{\text{Gauss}}{=}-\left( \underbrace{\int_{\partial\Omega} v\nabla u \cdot n \text{ }dS}_{= 0, v \in H_{0}^1(\Omega)}-\int_{\Omega}\nabla u^T\nabla vdx\right)=\int_{\Omega}\nabla u^T \nabla vdx \stackrel{!}{=}\lambda\int_{\Omega}e^u v dx.
$$

##### (ii) Existence of solution
We prove this by using Banachs fixed point theorem.

Let $S$ be the solution operator that maps $v \in C(\bar{\Omega})$ to the solution $u_{v}$of the following problem
$$
\begin{cases}
-\Delta u_{v} = \lambda e^v \quad \text{ in } \Omega, \\
u_{v} = 0 \quad \text{ on } \partial \Omega
\end{cases}
$$

This Operator is well defined because of the following theorem (theory of linear elliptic PDEs) and because for $v \in C(\bar{\Omega})$,  $\forall p: e^v \in L^p(\Omega)$.
![[Pasted image 20260414223941.png]]
We therefore know, that $u \in W^{2,p}(\Omega)\cap H_{0}^1(\Omega)$.
For $p > \frac{n}{2}$, we get $W^{2,p}(\Omega) \hookrightarrow C(\bar{\Omega})$ continously, so $S:C(\bar{\Omega})\to C(\bar{\Omega})$.
![[Pasted image 20260414221705.png]]
For a fixed $1>\delta >0$, we restrict $S$ onto $K=K{^{C(\bar{\Omega})}}_{\delta}(0)$.
Clearly, this set is closed, so $(K,||.||_{\infty})$ is a Banach space.
Let $v \in K$, $u_{v} = S(v)$.
So $||u_{v}||_{W^{2,p}(\Omega)}\leq C \lambda ||e^v||_{L^p(\Omega)}\leq$ because of Theorem 2.7 and $||u||_{\infty}\leq \tilde{C}||u||_{W^{2,p}}(\Omega)$ because of the embedding.
We get 
$$
||u||_{\infty}\leq C_{1} \lambda ||e^v||_{L^p(\Omega)}
$$
Pointwise, it holds, that $|e^v|\leq e^\delta$, so 
$$
||u||_{\infty}\leq C_{1} \lambda e^\delta \text{mass }(\Omega)^{1/p} \stackrel{!}{\leq}\delta \iff \lambda\leq \frac{\delta}{e^\delta C_{1} \text{ mass }(\Omega)^{1/p}}
$$
If we choose $\lambda$ accordingly, we get $S:K\to K$.

Let $v_{1},v_{2} \in K$, $u_{1}=S(v_{1}),u_{2}=S(v_{2})$, then
$$
||S(v_{1})-S(v_{2})||_{\infty}=||u_{1}-u_{2}||_{\infty}\leq \tilde{C}||u_{1}-u_{2}||_{W^{2,p}(\Omega)}\leq C_{1}\lambda||e^{v_{1}}-e^{v_{2}}||_{L^p(\Omega)}
$$
On $[-\delta,\delta]$, we get, using the mean value theorem for $x_{1},x_{2} \in[-\delta, \delta], \xi$ inbetween $x_{1}$ and $x_{2}$:
$$
|e^{x_{1}}-e^{x_{2}}|=e^{\xi}|x_{1}-x_{2}|\leq e^\delta|x_{1}-x_{2}|
$$

It follows, that
$$
||e^{v_{1}}-e^{v_{2}}||^p_{L^p(\Omega)}=\int_{\Omega}|e^{v_{1}}-e^{v_{2}}|^pdx\leq \int_{\Omega}(e^\delta |v_{1}-v_{2}| )^pdx=e^{\delta p}||v_{1}-v_{2}||^p_{L^p(\Omega)}
$$
and
$$
||S(v_{1})-S(v_{2})||_{\infty}\leq C_{1} \lambda e^\delta ||v_{1}-v_{2}||_{L^p(\Omega)}\leq C_{1} \lambda e^\delta \text{ mass}(\Omega)
^{1/p}||v_{1}-v_{2}||_{\infty}.$$
Because we already chose $\lambda$ correctly, this is a strict contraction.

By Banachs fixed point theorem, the Solution operator has an unique fixed point in $K$, so we have a solution for our problem.

##### (iii) Uniqueness of solution

#### (b)
Prove that $u_{\lambda}\geq 0$ almost everywhere in $\Omega$.
![[Pasted image 20260414232548.png]]
Let $w:=-u_{\lambda}$
We have $w = 0$ on $\partial \Omega$ and $-\Delta w=-\Delta(-u_{\lambda})=\Delta u_{\lambda}=-\lambda e^{u_{\lambda}}\leq 0$ in $\Omega$.
It follows, that $w=-u_{\lambda}\leq 0$ almost everywhere or $u_{\lambda} \geq 0$ almost everywhere.

#### (c)
Assuming that the problem has a solution $u_λ$ for every $λ > 0$, prove that $$∥u_{\lambda}∥_{H^1(Ω)} → +∞ \text{ as } λ → +∞.$$
We know, because $u_{\lambda}\geq 0$ almost everywhere
$$
-\Delta u_{\lambda}=\lambda e^{u_{\lambda}} \geq \lambda
$$
almost everywhere.

Consider
$$
\begin{cases}
-\Delta v = 1 \quad \text{ in } \Omega \\
v = 0 \text{ on } \partial \Omega
\end{cases}
$$
This is linear and has an unique, non trivial solution.
Multiplying the whole equation with $\lambda$, we get
$$
\begin{cases}
-\Delta(\lambda z)=\lambda \quad \text{ in } \Omega\\
\lambda z = 0\quad \text{ on }\partial \Omega
\end{cases}
$$
So we have for $w:=u_{\lambda}-\lambda v$
$$
-\Delta w=-\Delta(u_{\lambda}-z)\geq0
$$
Because of the weak maximum principle, we get $w\geq 0$ or
$u_{\lambda}\geq \lambda z$, and analogous to (b), $\lambda z\geq 0$ almost everywhere.
Because $z \neq 0$, the norm tends to infinity.
