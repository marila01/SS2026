Consider the following quasilinear parabolic problem
$$
\begin{cases}
\partial_{t}u-\text{div}(a(u)\nabla u)=|\nabla u| \text{ in } \Omega_{T} \\
u(x,t)= 0 \text{ on } \partial \Omega \times(0,T) \\
u(x,0)= u_{0}(x) \text{ in }\Omega
\end{cases}
$$
Let $X = L^2(0,T;H_{0}^1(\Omega))$. We define the operator $\mathcal{A}:X\to X'$ by:
$$
\langle \mathcal{A}u,v\rangle_{X',X}=\int_{0}^T\int_{\Omega}a(u)\nabla u\cdot \nabla v
\,dx\,dt - \int_{0}^T\int_{\Omega}|\nabla u|v\,dx\,dt
$$
Assume $a:\mathbb{R} \to \mathbb{R}$ is smooth and strictly positive, satisfying $0< \alpha \leq a(s)\leq \beta$ for all $s \in \mathbb{R}$.
![[Pasted image 20260624104048.png]]
### (a)
Is the operator $\mathcal{A}$ monotone on $X$?

No.
Let $n =1$, $\Omega=(0,2\pi)$, $T>0$, $a=1$.
$a$ is smooth and $0<1\leq a(s)\leq 1$.
Let $u(x,t)=\sin\left( \frac{x}{2} \right)$, $v(x,t)= 0$.
Then $u,v \in X$.
If $\mathcal{A}$ was monotone, then
$$
\langle \mathcal{A}u-\mathcal{A}v,u-v\rangle \geq 0
$$
Because $v= 0$, $\mathcal{A}v= 0$. 
We calculate
$$
\langle \mathcal{A}u,u\rangle = \int_{0}^T \int_{0}^{2\pi}|u_{x}|^2\,dx\,dt- \int_{0}^T \int_{0}^{2\pi}|u_{x}|u\,dx\,dt,
$$
with $u_{x}(x,t)=\frac{1}{2}\cos\left( \frac{x}{2} \right)$.
We now solve the first integral, substituting $\frac{x}{2}$
$$
\int_{0}^{2\pi}|u_{x}|^2\,dx = \frac{1}{2}\int_{0}^\pi \cos(u)^2\,du = \frac{\pi}{4}
$$
and, once again substituting $\frac{x}{2}$, we obtain for the second integral
$$
\int_{0}^{2\pi}|u_{x}|u\,dx=\int_{0}^\pi |\cos u|\sin u\,du = \int_{0}^{\pi/2}\cos u \sin u\,du + \int_{\frac{\pi}{2}}^\pi (-\cos u)\sin u \, du = \frac{1}{2}+\frac{1}{2} = 1.
$$
Putting everything together, we get
$$
\langle \mathcal{A}u-\mathcal{A}v, u-v \rangle = T \left(  \frac{\pi}{4}-1 \right)<0.
$$

### (b)
Is the operator $\mathcal{A}$ coercive on $X$?
Yes, if $\alpha > C_{p}$. Using Hölder, the lower bound for $a$, and Poincare, we get
$$
\begin{align}
\langle \mathcal{A}u,u
\rangle &\geq \int_{0}^T\int_{\Omega}|a(u)||\nabla u|^2\,dx\,dt-\int_{0}^T\int_{\Omega} |\nabla u||u|\,dx\,dt\\
&\geq \int_{0}^T \alpha ||\nabla u(t)||^2_{L^2} - ||\nabla u(t)||_{L^2}||u(t)||_{L^2}\,dt \\
&\geq \int_{0}^T (\alpha-C_{p})||\nabla u(t)||^2_{L^2}\,dt \\
&\geq (\alpha-C_{p})C||u||_{X}^2
\end{align}
$$
which gives us coercivity.

If we cannot bound the Poincare-constant in such a way, we dont get coercivity:
Again, Let $\Omega=(0,2\pi)$, $a(s)=1$,
Let $u_{k}(x,t)=k\sin\left( \frac{x}{2} \right) \in X$.
Then, as above
$$
\langle \mathcal{A}u_{k},u_{k}\rangle = T k^2 \left( \frac{\pi}{4}-1 \right)\to -\infty
$$
but $||u_{k}||_{X}\to \infty$.
