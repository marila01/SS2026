Consider the porous medium equation 
$$
u_{t}= \Delta(u^m), x \in \mathbb{R}^n, t> 0, m >1
$$
### a)
Let $u_{\lambda}(x,t):=\lambda^\alpha u(\lambda^\beta x,\lambda t)$. Determine the relation between $\alpha$ and $\beta$ for which, if $u$ is a strong solution, the also $u_{\lambda}$ is again a strong solution.

Let $y:= \lambda^\beta x, s:=\lambda t$.
Then
$$
\partial_{x_{i}}[u_{\lambda}(x,t)^m]=\lambda^{\alpha m+\beta}\partial_{y_{i}}(u^m)(y,s)
$$
and
$$
\partial_{x_{i}}^2[u_{\lambda}(x,t)^m]=\lambda^{\alpha m+ 2\beta}\partial_{y_{i}}^2(u^m)(y,s)
$$
which gives
$$
\Delta(u_{\lambda}^m)(x,t)= \lambda^{\alpha m+2\beta}\Delta(u^m)(y,s).
$$
Taking the time-derivative, we get
$$
(u_{\lambda})_{t}(x,t)=\lambda^{\alpha+1}u_{s}(y,s)
$$
We want
$$
(u_{\lambda})_{t}=\lambda^{\alpha+1}u_{s}\stackrel{!}{=}\lambda^{\alpha m+2\beta}\Delta (u^m)=\Delta(u_{\lambda}^m),
$$
which is the case if $\alpha+1=\alpha m+2\beta$.

### b)
Assume in addition, that the total mass is preserved under the scaling, i.e.
$$
\int_{\mathbb{R}^n}u_{\lambda}(x,\lambda)dx=\int_{\mathbb{R}^n}u(x,t)dx.
$$
Show that, then
$$
\alpha= \frac{n}{n(m-1)+2},\quad \beta=\frac{1}{n(m-1)+2}.
$$

Let $M(t):= \int_{\mathbb{R}^n}u(x,t)dx$. Using the Transformation-formlula for $y:=\lambda^\beta x$, we get
$$
M(t)=\int_{\mathbb{R}^n}u(x,t)dx=\int_{\mathbb{R}^n}u_{\lambda}(x,t)dx = \lambda^{\alpha-n\beta}\int_{\mathbb{R}^n}u(y,\lambda t)dy=\lambda^{\alpha-n\beta}M(\lambda t).
$$
We need, that $M$ is constant in time to conclude the argument.
To use the PDE, we assume that everything is regular enough (i.e. $u(.,t) \in L^1(\mathbb{R}^n)$, $u_{t}(.,t)\in L^1(\mathbb{R}^n)$, $u^m \in L^1(\mathbb{R}^n)$, we can take time derivatives, switch limits etc., everything continous in time etc.)
Take $\phi$ such that $\phi = 1$ in $B_{1}(0)$, $\phi = 0$ for $x \in \mathbb{R}^n \setminus B_{2}(0)$ and $\phi \in C_{0}^\infty(\mathbb{R}^n)$.
Let $\phi_{R}(x):=\phi\left( \frac{x}{R} \right)$.
We take the time derivative of the integral and test our PDE with this
$$
\frac{\mathrm{d}}{\mathrm{d}t}\int_{\mathbb{R}^n}u(x,t)\phi_{R}(x)dx = \int_{\mathbb{R}^n}u_{t}(x,t)\phi_{R}(x)dx = \int_{\mathbb{R}^n}\Delta( u^m) \phi_{R}(x)dx 
$$
We know $|\Delta\phi_{R}(x)| \leq \frac{C}{R^2}$ uniformly for some constant $C>0$ and assume we can partially integrate.
This gives us
$$
| \int_{\mathbb{R}^n}\Delta (u^m) \phi_{R}dx|  = |\int_{\mathbb{R}^n} u^m \Delta \phi_{R}dx|\leq \int_{\mathbb{R}^n}|u|^mdx \frac{C}{R^2}
$$
which goes to $0$ as $R\to \infty$.
Because we assumed that $u_{t} \in L^1(\mathbb{R}^n)$, we can also take the limit on the LHS and switch them with the integrals.
This gives us
$$
M'(t)= 0.
$$
We get 
$$
M(t)=M(\lambda t)
$$
and from the transformation formula
$\alpha=n\beta$.
Plugging this into the equation from a), we are done.

### c)
Consider the definition of the weak solution provided by the Skriptum in Definition 3.27. Assuming $u_{0} = 0$, is it still true that if $u$ is a weak solution, then $u_{\lambda}$ is also a weak solution?

![[Pasted image 20260623173658.png]]

Yes but actually no.
We can show that the only solution with $u(0)=0$ is $u=0$, but then also $u_{\lambda}= 0$.
![[Pasted image 20260623195709.png]]
the beweis in question :
![[Pasted image 20260623195828.png]] 

![[Pasted image 20260623200133.png]]