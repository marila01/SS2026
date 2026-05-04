#### 1: Show that $a(0)=0$
Since $0\in L^2(\mathbb{R})$, the image of $0$  must again belong to $L^2(\mathbb{R})$. But
$$
a\circ 0 = a(0)
$$
is just the constant function with value $a(0)$. A constant function belongs to $L^2(\mathbb{R})$ only if it is zero.
So we only need to show, that $a$ is linear.

#### 2: Construct weakly convergent sequence
Fix $x,y\in\mathbb{R}$. For every $n\in\mathbb{N}$, define $u_n:\mathbb{R}\to\mathbb{R}$ by
$$
u_n(t):=
\begin{cases}
x, & t\in \left[\frac{k}{2^n},\frac{k+1}{2^n}\right) \text{ for } k \text{ even},\\[0.4em]
y, & t\in \left[\frac{k}{2^n},\frac{k+1}{2^n}\right) \text{ for } k \text{ odd},
\end{cases}
\qquad t\in[0,1],
$$
and set $u_n(t)=0$ for $t\notin[0,1]$. (We want something, that alternates wildly)

Then each $u_n\in L^2(\mathbb{R})$, and the sequence $(u_n)$ is bounded in $L^2(\mathbb{R})$, because
$$
|u_n(t)|\leq \max\{|x|,|y|\}\mathbf 1_{[0,1]}(t).
$$

We claim that
$$
u_n \rightharpoonup \frac{x+y}{2}\mathbf 1_{[0,1]}
\qquad\text{weakly in }L^2(\mathbb{R}).
$$  
  
To prove this, let  
$$  
m:=\frac{x+y}{2}.  
$$  
Then $u_n-m\mathbf 1_{[0,1]}$ is supported in $[0,1]$, and on each interval  
$$  
I_{k,n}:=\left[\frac{k}{2^n},\frac{k+1}{2^n}\right)  
$$  
we have  
$$  
u_n-m=  
\begin{cases}  
\frac{x-y}{2}, & \text{if }k\text{ is even},\\[0.4em]  
-\frac{x-y}{2}, & \text{if }k\text{ is odd}.  
\end{cases}  
$$  
For every $\varphi\in L^2(\mathbb{R})$,  
$$  
\int_{\mathbb{R}}\bigl(u_n(t)-m\mathbf 1_{[0,1]}(t)\bigr)\varphi(t)\,dt  
=  
\frac{x-y}{2}\sum_{k=0}^{2^n-1}(-1)^k\int_{I_{k,n}}\varphi(t)\,dt.  
$$  
  
Now group neighboring intervals in pairs. For $j=0,\dots,2^{n-1}-1$, set  
$$  
J_{j,n}:=I_{2j,n}\cup I_{2j+1,n}  
=  
\left[\frac{2j}{2^n},\frac{2j+2}{2^n}\right).  
$$  
Then  
$$  
\sum_{k=0}^{2^n-1}(-1)^k\int_{I_{k,n}}\varphi(t)\,dt  
=  
\sum_{j=0}^{2^{n-1}-1}  
\left(  
\int_{I_{2j,n}}\varphi(t)\,dt-\int_{I_{2j+1,n}}\varphi(t)\,dt  
\right).  
$$  
Therefore,  
$$  
\left|  
\int_{\mathbb{R}}\bigl(u_n-m\mathbf 1_{[0,1]}\bigr)\varphi  
\right|  
\le  
\frac{|x-y|}{2}  
\sum_{j=0}^{2^{n-1}-1}  
\left|  
\int_{I_{2j,n}}\varphi-\int_{I_{2j+1,n}}\varphi  
\right|.  
$$  
  
At this point we first consider $\varphi\in C([0,1])$. Since $\varphi$ is uniformly continuous on $[0,1]$, its modulus of continuity  
$$  
\omega_\varphi(\delta):=\sup\{|\varphi(s)-\varphi(t)|:s,t\in[0,1],\ |s-t|\le \delta\}  
$$  
satisfies $\omega_\varphi(\delta)\to 0$ as $\delta\to 0$. For $t\in I_{2j,n}$ and $s\in I_{2j+1,n}$, we have  
$|t-s|\le 2^{-n}$, and    
$$|\varphi(t)-\varphi(s)|\le \omega_\varphi(2^{-n}).  
$$ 
Using the translation $s=t+2^{-n}$, we obtain  
$$  
\left|  
\int_{I_{2j,n}}\varphi(t)\,dt-\int_{I_{2j+1,n}}\varphi(t)\,dt  
\right|  
=  
\left|  
\int_{I_{2j,n}}\bigl(\varphi(t)-\varphi(t+2^{-n})\bigr)\,dt  
\right|  
\le  
2^{-n}\omega_\varphi(2^{-n}).  
$$  
Summing over $j$ yields  
$$  
\left|  
\int_{\mathbb{R}}\bigl(u_n-m\mathbf 1_{[0,1]}\bigr)\varphi  
\right|  
\le  
\frac{|x-y|}{2}\,2^{n-1}\cdot 2^{-n}\omega_\varphi(2^{-n})  
=  
\frac{|x-y|}{4}\,\omega_\varphi(2^{-n}).  
$$  
Since $\omega_\varphi(2^{-n})\to 0$, it follows that  
$$  
\int_{\mathbb{R}}u_n(t)\varphi(t)\,dt  
\longrightarrow  
\int_{\mathbb{R}}m\mathbf 1_{[0,1]}(t)\varphi(t)\,dt  
\qquad  
\text{for every }\varphi\in C([0,1]).  
$$
  
Let $\psi\in L^2(\mathbb{R})$ be arbitrary. Since $C([0,1])$ is dense in $L^2([0,1])$, choose $\varphi_\ell\in C([0,1])$ such that  
$$  
\varphi_\ell\to \psi|_{[0,1]}  
\qquad\text{in }L^2([0,1]).  
$$  
Because $(u_n)$is uniformly bounded in $L^2(\mathbb{R})$, say  
$$  
\|u_n\|_{L^2(\mathbb{R})}\le C  
\qquad\text{for all }n,  
$$  
we obtain  
$$  
\left|  
\int_{\mathbb{R}}u_n(\psi-\varphi_\ell)  
\right|  
\le  
\|u_n\|_{L^2}\,\|\psi-\varphi_\ell\|_{L^2([0,1])}  
\le  
C\|\psi-\varphi_\ell\|_{L^2([0,1])}.  
$$  
Similarly,  
$$  
\left|  
\int_{\mathbb{R}}m\mathbf 1_{[0,1]}(\psi-\varphi_\ell)  
\right|  
\le  
|m|\,\|\mathbf 1_{[0,1]}\|_{L^2}\,\|\psi-\varphi_\ell\|_{L^2([0,1])}.  
$$  
Hence, first letting $n\to\infty$ for fixed $\ell$, and then $\ell\to\infty$, we conclude that  
$$  
\int_{\mathbb{R}}u_n(t)\psi(t)\,dt  
\longrightarrow  
\int_{\mathbb{R}}m\mathbf 1_{[0,1]}(t)\psi(t)\,dt  
\qquad  
\forall \psi\in L^2(\mathbb{R}).  
$$  
This proves  
$$  
u_n \rightharpoonup \frac{x+y}{2}\mathbf 1_{[0,1]}  
\qquad\text{in }L^2(\mathbb{R}).  
$$
## Step 3: Apply weak sequential continuity

By weak sequential continuity of the superposition operator, the weak convergence of \(u_n\) implies
$$
a(u_n)\rightharpoonup a\!\left(\frac{x+y}{2}\mathbf 1_{[0,1]}\right)
\qquad\text{in }L^2(\mathbb{R}).
$$
Since \(a(0)=0\), we have
$$
a\!\left(\frac{x+y}{2}\mathbf 1_{[0,1]}\right)
=
a\!\left(\frac{x+y}{2}\right)\mathbf 1_{[0,1]}.
$$

On the other hand, by construction,
$$
a(u_n)(t)=
\begin{cases}
a(x), & t\in \left[\frac{k}{2^n},\frac{k+1}{2^n}\right) \text{ for } k \text{ even},\\[0.4em]
a(y), & t\in \left[\frac{k}{2^n},\frac{k+1}{2^n}\right) \text{ for } k \text{ odd},
\end{cases}
\qquad t\in[0,1],
$$
and \(a(u_n)(t)=0\) for \(t\notin[0,1]\). Exactly the same argument as before shows that
$$
a(u_n)\rightharpoonup \frac{a(x)+a(y)}{2}\mathbf 1_{[0,1]}
\qquad\text{weakly in }L^2(\mathbb{R}).
$$

By uniqueness of the weak limit,
$$
a\!\left(\frac{x+y}{2}\right)\mathbf 1_{[0,1]}
=
\frac{a(x)+a(y)}{2}\mathbf 1_{[0,1]}.
$$
Therefore,
$$
a\!\left(\frac{x+y}{2}\right)=\frac{a(x)+a(y)}{2}
\qquad\forall x,y\in\mathbb{R}.
$$

Thus \(a\) satisfies the midpoint identity.

## Step 4: Extend the midpoint identity

We now show that for every dyadic number \(\lambda=\frac{k}{2^n}\in[0,1]\),
$$
a(\lambda x+(1-\lambda)y)=\lambda a(x)+(1-\lambda)a(y).
$$
This follows by induction on \(n\), using the midpoint identity repeatedly.

Since the dyadic numbers are dense in \([0,1]\), and \(a\) is continuous, we may pass to the limit and obtain
$$
a(\lambda x+(1-\lambda)y)=\lambda a(x)+(1-\lambda)a(y)
\qquad\forall x,y\in\mathbb{R},\ \forall \lambda\in[0,1].
$$

## Step 5: Conclude linearity

Setting \(y=0\) and using \(a(0)=0\), we get
$$
a(\lambda x)=\lambda a(x)
\qquad\forall x\in\mathbb{R},\ \forall \lambda\in[0,1].
$$
In particular, with \(\lambda=\frac12\),
$$
a(x+y)
=
2\,a\!\left(\frac{x+y}{2}\right)
=
2\cdot \frac{a(x)+a(y)}{2}
=
a(x)+a(y).
$$
So \(a\) is additive.

Since \(a\) is additive and continuous, it follows that \(a\) is linear. Hence there exists \(c\in\mathbb{R}\) such that
$$
a(t)=ct
\qquad\forall t\in\mathbb{R}.
$$

Therefore \(a\) is affine; more precisely, because \(a(0)=0\), it is in fact linear.

## Conclusion

Every continuous function \(a:\mathbb{R}\to\mathbb{R}\) such that the associated superposition operator
$$
u\mapsto a\circ u
$$
is weakly sequentially continuous on \(L^2(\mathbb{R})\) must be of the form
$$
a(t)=ct
\qquad\forall t\in\mathbb{R}.
$$