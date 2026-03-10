$\forall u_{0} \in U\forall \xi \in X$ gilt: $\delta \mathcal{F}(u_{0},\xi)$ existiert.

**Beweis:**
Der $1-Graph(u_{0})$ ist kompakt, $V$ offen, d.h. $\exists \delta >0$ sodass
$$
1-Graph(u)\subset V \quad \forall v \in B_{\delta}(u_{0},X):=\{ v \in X | ||u_{0}-v||_{X}< \delta \},
$$
![[Pasted image 20260309193220.png]]
Da $||w||_{C^1(\bar{\Omega};\mathbb{R}^n)}=\mathrm{sup}_{x \in \Omega}\mathrm{max}(|w(x)|,|Dw(x)|)$
$$
\implies \phi(\varepsilon):=\mathcal{F}(u_{0}+\varepsilon \xi)
$$
ist definiert für jedes (feste) $\xi \in X$ und $|\varepsilon|<\varepsilon_{0}=\frac{\delta}{1+||\xi||_{X}}$.
Da $\Omega$ beschränkt und $F \in C^1(V;\mathbb{R})$
$$
\implies \phi \in C^1(-\varepsilon_{0},\varepsilon_{0}) \implies \delta \mathcal{F}(u_{0},\xi)=\phi'(0) \text{ existiert.}
$$
