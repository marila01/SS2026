Prove the equality on page 60 of the lecture notes.
So, prove for $z(t):=\int u(t,x)w_{1}(x)dx$, $t\geq 0$.
$$
\frac{\mathrm{d}}{\mathrm{d}t} z(t)=
\frac{\mathrm{d}}{\mathrm{d}t}\langle u,w_{1} \rangle_{H^{-1},H_{0}^1}= \langle u_{t},w_{1} \rangle_{H^{-1},H_{0}^1} .  
$$
*Proof:*
Let $T>0$ and let $w_1\in H_0^1(\Omega)$ be fixed. Define
$$
z(t):=\int_\Omega u(t,x)w_1(x)\,dx,
\qquad t\in(0,T).
$$
Using the duality between $H^{-1}(\Omega)$ and $H_0^1(\Omega)$, we write
$$
z(t)=\langle u(t),w_1\rangle_{H^{-1},H_0^1}.
$$
We want to prove that
$$
z'(t)=\langle u_t(t),w_1\rangle_{H^{-1},H_0^1}
$$
in the sense of distributions on $(0,T)$. Later we will find out that this also holds in a strong sense.

Let
$$
\ell_{w_1}:H^{-1}(\Omega)\to \mathbb R
$$
be defined by
$$
\ell_{w_1}(v):=\langle v,w_1\rangle_{H^{-1},H_0^1}.
$$
Since $w_1\in H_0^1(\Omega)$ is fixed, $\ell_{w_1}$ is continuous, linear and real-valued (on $H^{-1}(\Omega)$). Also,
$$
z(t)=\ell_{w_1}(u(t)).
$$
Let $\varphi\in C_c^\infty(0,T)$. Since $u_t$ is the weak time derivative of $u$ with values in $H^{-1}(\Omega)$, we have
$$
-\int_0^T u(t)\varphi'(t)\,dt
=
\int_0^T u_t(t)\varphi(t)\,dt
$$
in $H^{-1}(\Omega)$. Applying $\ell_{w_1}$ (linear, continuous) and using the homogeneity of $\ell_{w_{1}}$ for $\varphi$ and $\varphi'$ yields
$$
-\int_0^T \ell_{w_1}(u(t))\varphi'(t)\,dt
=
\int_0^T \ell_{w_1}(u_t(t))\varphi(t)\,dt.
$$
Using the definitions of $z$ and $\ell_{w_1}$, this becomes
$$
-\int_0^T z(t)\varphi'(t)\,dt
=
\int_0^T 
\langle u_t(t),w_1\rangle_{H^{-1},H_0^1}
\varphi(t)\,dt.
$$
This is the definition of the distributional derivative of $z$, so we get
$$
\frac{d}{dt}z(t)
=
\frac{d}{dt}\langle u(t),w_1\rangle_{H^{-1},H_0^1}
=
\langle u_t(t),w_1\rangle_{H^{-1},H_0^1}
$$
in $\mathcal D'(0,T)$. 
In our case, the R.H.S. is continuous, so this becomes a pointwise equality (for a representative).
![[Pasted image 20260512232614.png]]
