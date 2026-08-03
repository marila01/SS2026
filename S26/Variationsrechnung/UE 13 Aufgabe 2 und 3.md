Für die nächsten beiden Aufgaben betrachten wir folgendes Setting. Sei $\Omega \subset \mathbb{R}^d$ eine offene, beschränkte Menge mit Lipschitz-Rand und $Y = \mathbb{R}^d\setminus \mathbb{Z}^d$ der $d-$dimensionale Torus. 
Gegeben sei
$$
a \in L^\infty(\Omega \times Y, \mathbb{R}^{m \times m}_{\text{sym}}), \quad \exists \alpha > 0: \forall \xi \in \mathbb{R}^m \text{ f. ü.  in }\Omega:  \xi^T a(x,y)\xi \geq \alpha |\xi|^2.
$$
Für $\varepsilon >0$ definieren wir
$$
C_{\varepsilon}(x):=\varepsilon\left(  \left\lfloor  \frac{x}{\varepsilon}  \right\rfloor +[0,1)^d \right), \quad a^\varepsilon(x):= \frac{1}{\varepsilon^d}\int_{C_{\varepsilon}(x)}a\left( w, \frac{x}{\varepsilon} \right)\,dw,
$$
Weiter seien die homogenisierten Koeffizienten definiert durch
$$
a^*(x):=\int_{Y}a(x,y)\,dy,\quad a_{*}(x):=\left( \int_{Y}a(x,y)^{-1}\,dy \right)^{-1}.
$$
Betrachte die folgenden quadratische Funktionale auf $L^2(\Omega, \mathbb{R}^m)$:
$$
F_{\varepsilon}(u):=\int_{\Omega}u(x)^Ta^\varepsilon(x)u(x)\,dx,
$$
$$
F^*(u):=\int_{\Omega}u(x)^Ta^*(x)u(x)\,dx,
$$
$$
F_{*}(u):= \int_{\Omega}u(x)^T a_{*}(x)u(x)\,dx.
$$

# 2)
Zeige, dass in der starken $L^2$-Topologie gilt $\Gamma-\lim_{ \varepsilon \to 0 }F_{\varepsilon}=F^*$.

# 3)
Zeige, dass in der starken $L^2$-Topologie gilt  $\Gamma-\lim_{ \varepsilon \to 0 }F_\varepsilon = F_{*}$.

