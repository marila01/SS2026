---
sticker: emoji//1f613
---
Let $\Omega \subset \mathbb{R}^n$ be a bounded domain with smooth boundary. Consider the problem
$$
\begin{cases}
-\Delta u(x) = \lambda \int_{\Omega}K(x,y)u(y)dy+f(x), \quad x \in \Omega \\
u = 0, \quad \text{ on } \partial \Omega,
\end{cases}
$$
where
- $\lambda \in \mathbb{R}$
- $f \in L^2(\Omega)$
- $K \in L^2(\Omega \times \Omega)$.
Define the operator $\mathcal{K}: L^2(\Omega)\to L^2(\Omega)$ by
$$
(\mathcal{K}u)(x):=\int_{\Omega}K(x,y)u(y)dy.
$$
Under which (non-trivial) conditions on $λ$ and $∥K∥_{L^2(Ω×Ω)}$ does the problem above admit a weak solution? Under which conditions can you guarantee that such a solution is unique?

We show existence and uniqueness with Lax-Milgram.
First, we need the weak formulation:
We want $u \in H_{0}^1(\Omega)$ such that $\forall v \in H_{0}^1(\Omega)$, it holds, that
$$
\int_{\Omega}-(\Delta u )wdx = \int_{\Omega}\nabla u^T\nabla wdx=\int_{\Omega}\left( \lambda \int_{\Omega}K(x,y)u(y)dy+f(x) \right)wdx
$$
Define
$$
a(u,w):= \int_{\Omega}(\nabla u(x)^T\nabla w(x)-\lambda \int_{\Omega}K(x,y)u(y)w(x)dy)dx
$$
which is bilinear by definition.

First, we show, that this bilinear form is continous by repeatedly using Cauchy-Schwartz:
$$
|a(u,w)|\leq ||\nabla u||_{L^2(\Omega)}||\nabla w||_{L^2(\Omega)}+ |\lambda|||K||_{L^2(\Omega \times \Omega)}||u||_{L^2(\Omega)}||w||_{L^2(\Omega)}\leq (1+|\lambda| ||K||_{L^2(\Omega \times \Omega)})||u|_{H_{0}^1(\Omega)}||w||_{H_{0}^1(\Omega)}.
$$
Now, we need to show, that  $a$ is coercive:
$$
a(u,u)
= \int_{\Omega}\left( |\nabla u|^2-\lambda \int_{\Omega}K(x,y)u(y)u(x)dy \right)dx
 \geq \int_{\Omega}|\nabla u|^2dx-|\lambda| ||K||_{L^2(\Omega \times \Omega)} ||u(x)u(y)||_{L^2(\Omega \times \Omega)}
= ||\nabla u ||^2_{L^2(\Omega)}-|\lambda| ||K||_{L^2(\Omega \times \Omega)}||u||^2_{L^2(\Omega)} 
\geq (1-|\lambda| ||K||_{L^2(\Omega \times \Omega)}C_{p}^2)||\nabla u||^2_{L^2(\Omega)}
\geq \frac{1-|\lambda| ||K||_{L^2(\Omega \times \Omega)}C_{p}^2}{1+C_{p}^2} ||u||_{H_{0}^1(\Omega)}^2
$$
This constant is $> 0$, if $|\lambda|||K||_{L^2(\Omega \times \Omega)}C_{p} ^2 < 1$.
Also, $\ell(w):=\int_{\Omega}fwdx$ is continous because of Cauchy-Schwartz and $f,w \in L^2(\Omega)$.

So Lax-Milgram gives us Existence and Uniqueness of solutions.


We get existence but not uniqueness, if $f$ is in the Range of the Operator 
$$
-\Delta+\lambda\mathcal{K}
$$
but $\ker (-\Delta+\lambda\mathcal{K})\neq \{ 0 \}$.
One could show that with Schauder. I'm not doing that.