Let $k \in \mathbb{N}$, and let $A_{\alpha}\in \mathbb{R}^{n \times n}$ for every $\alpha \in \mathbb{N}^d$ with $|\alpha|=k\in \mathbb{N}$.
We definine the $k$-th order differential operator by
$$
\mathcal{A}:=\sum_{|\alpha|=k}A_{\alpha}\partial^\alpha.
$$
We denote its symbol by 
$$
\mathbb{A}(\xi):= \sum_{|\alpha|=k}A_{\alpha}\xi^\alpha
$$
for $\xi \in \mathbb{R}^d$ and $\xi^\alpha:=\xi_{1}^{\alpha_{1}}\cdot\dots \cdot \xi_{d}^{\alpha_{d}}$.
We assume $\mathcal{A}$ is elliptic, i.e. we have 
$$
\mathbb{A}(\xi) \text{ is  invertible}
$$
for every $\xi \in \mathbb{R}^d\setminus \{ 0 \}$.
Show that:
**(a):**
$\mathbb{A}^{-1}(\xi)$ is a rational matrix-valued function with pole in $0$, i.e.,
$$
\mathbb{A}^{-1}(\xi)=\frac{1}{q(\xi)}P(\xi)
$$
holds for a $k(n-1)$-homogenous matrix-valued polynomial $P$ and a $kn$-homogenous realvalued polynomial $q$.

*Proof:* 
We know that for $\xi\neq 0$. the matrix $\mathbb{A}(\xi)$ is invertible, so $\det\mathbb{A}(\xi)\neq 0$.
From linear algebra, we get
$$
\mathbb{A}^{-1}(\xi)= \frac{1}{\det(\mathbb{A}(\xi))}(\text{cof}(\mathbb{A}(\xi)))^T
$$
with $\text{cof}(\mathbb{A}(\xi))_{ij}=(-1)^{i+j}\det(\mathbb{A}(\xi)^{ij})$.
$\mathbb{A}(\xi)^{ij}$ denotes the Matrix, where we leave out the $i$-th row and the $j$-th column.

First, we note, that 
$$\mathbb{A}(\lambda\xi)=\sum_{|\alpha|=k}A_{\alpha}(\lambda \xi_{1})^{\alpha_{1}}\cdot\dots \cdot(\lambda \xi_{d})^{\alpha_{d}}=\lambda^k\mathbb{A}(\xi)$$
Also, $\mathbb{A}$ is a matrix-valued polynomial in $\xi$.

We also know, that $\det(\mathbb{A(\xi)})$ is $kn$-homogenous, because
$$
\det(\mathbb{A}(\lambda \xi))=\det(\lambda^k\mathbb{A}(\xi))=(\lambda^k)^n\det(\mathbb{A}(\xi))
$$
because determinants are $n$-homogenous.
Every entry of $\mathbb{A}(\xi)$ is a real-valued polynomial in $\xi$, the determinant combines them to products/sums, so the determinant is also a real-values polynomial in $\xi$.

Consider $\text{cof}(\mathbb{A}(\xi))^T$. Per definition and the arguments from above, this is a matrix-valued polynomial in $\xi$. 
We only need to proof, that this polynomial is $(n-1)k$-homogenous.
For every $i,j=1,\dots, n$, we get
$$
(\text{cof}(\mathbb{A(\lambda \xi)}))^T_{ij}=\text{cof}(\mathbb{A}(\lambda \xi))_{ji}=(-1)^{i+j}\det(\mathbb{A}^{ji} (\lambda\xi))
$$
$\mathbb{A}^{ji}(\xi)$ has the same structure as $\mathbb{A}(\xi)$ only with dimension $n-1$.
We have already seen the $\det(\mathbb{A}^{ji}(\xi))$ is $(n-1)k$-homogenous, so 
$\text{cof}(\mathbb{A}(\xi))^T$ is $(n-1)k$-homogenous.
Because $\det(\mathbb{A}(0))=\det(0)=0$, we get a pole for $x=0$.

**(b):**
Infer from (a), that for two elliptic $k$-th order differential operators $\mathcal{A}_{1},\mathcal{A}_{2}$, there exists a constant $C> 0$ such that for all $\phi \in C_{c}^\infty(\mathbb{R}^d;\mathbb{R}^n)$
$$
||\mathcal{A}_{1}\phi||_{L^2(\mathbb{R}^d;\mathbb{R}^n)}\leq C||\mathcal{A}_{2}\phi||_{L^2(\mathbb{R}^d;\mathbb{R}^n)}.
$$

*Proof:*
We know, that $C_{c}^\infty(\mathbb{R}^d;\mathbb{R}^n) \subset\mathcal{S}(\mathbb{R}^d;\mathbb{R}^n)$ and $\mathcal{F}$ is an isometry w.r.t. the $L^2$-scalarproduct in this space.

Consider the Fourier-transform of $\mathcal{A_{1}}\phi$:
$$
\begin{align}
\mathcal{F}(\mathcal{A}_{1}\phi)(\xi)&=\mathcal{F}\left( \sum_{|\alpha|=k}A_{\alpha}\partial^\alpha \phi \right)(\xi) \\
&=\sum_{|\alpha|=k}A_{\alpha}\mathcal{F}(\partial ^\alpha \phi) (\xi)\\
&=\sum_{|\alpha|=k}A_{\alpha}i^{|\alpha|}\xi^\alpha \mathcal{F}(\phi)(\xi) \\
&= i^k\mathbb{A}_{1}(\xi)\mathcal{F}(\phi)(\xi).
\end{align}
$$
We also get $\mathcal{F}(\mathcal{A}_{2}\phi)=i^k\mathbb{A}_{2}(\xi)\mathcal{F}(\phi)\iff \mathcal{F}(\phi)=i^{-k}\mathbb{A}_{2}^{-1}(\xi)\mathcal{F}(\mathcal{A}_{2}\phi)$ for $\xi \neq 0$.
So for $\xi\neq 0$:
$$
\mathcal{F}(\mathcal{A}_{1}\phi)(\xi)=\mathbb{A}_{1}(\xi)\mathbb{A}_{2}^{-1}(\xi)\mathcal{F}(\mathcal{A}_{2}\phi)(\xi)
$$
We need to show, that
$$
\sup_{0 \neq \xi \in \mathbb{R}^d}||\mathbb{A}_{1}(\xi)\mathbb{A}_{2}^{-1}(\xi)||<\infty
$$
This Function is continous on $K_{1}(0)\setminus U_{1}(0)$ compact and thus bounded on the unit-sphere by a constant $C> 0$.
Because for every $0\neq\xi \in \mathbb{R}^d$, we can write $\xi=|\xi|\cdot \underbrace{\frac{\xi}{|\xi|}}_{\in K_{1}(0)\setminus U_{1}(0)}$, we can use (a).
$$
||\mathbb{A}_{1}(\xi)\mathbb{A}_{2}^{-1}(\xi)||=|| \mathbb{A}_{1}\left( \frac{\xi}{|\xi|} \right)\mathbb{A}_{2}^{-1}\left( \frac{\xi}{|\xi|} \right)||\leq C.
$$
Then
$$
\begin{align}
||\mathcal{F}(\mathcal{A}_{1}\phi)||_{L^2(\mathbb{R}^d;\mathbb{R}^n)}^2&=\int_{\mathbb{R}^d}|\mathcal{F}(\mathcal{A}_{1}\phi)(\xi)|^2d\xi \\
&=\int_{\mathbb{R}^d\setminus \{ 0 \}}|\mathcal{F}(\mathcal{A}_{1}\phi)(\xi)|^2d\xi\\
&=\int_{\mathbb{R}^d\setminus \{ 0 \}}|\mathbb{A}_{1}(\xi)\mathbb{A}_{2}^{-1}(\xi)\mathcal{F}(\mathcal{A}_{2}\phi)(\xi)|^2d\xi \\
&\leq \int_{\mathbb{R}^d\setminus \{ 0 \}}||\mathbb{A}_{1}(\xi)\mathbb{A}_{2}^{-1}(\xi)||^2|\mathcal{F}(\mathcal{A}_{2}\phi)(\xi)|^2d\xi \\
&\leq \sup_{\xi \in\mathbb{R}^d\setminus \{ 0 \}}||\mathbb{A}_{1}(\xi)\mathbb{A}_{2}^{-1}(\xi)||^2\int_{{\mathbb{R}^d\setminus \{ 0 \}}}|\mathcal{F}(\mathcal{A}_{2}\phi)(\xi)|^2d\xi \\
&=C^2||\mathcal{F}(\mathcal{A}_{2}\phi)||_{L^2(\mathbb{R}^d;\mathbb{R}^n)}^2.
\end{align}
$$


