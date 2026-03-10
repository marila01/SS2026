Generelle Annahmen für dieses Sub-Kapitel:
Sei $\Omega \subset \mathbb{R}^n$ offen, beschränkt; $u \in X:=C^1(\bar{\Omega};\mathbb{R}^N)$
$1-Graph(u):=\{ (x,u(x),Du(x))|x \in \underbrace{\bar{\Omega}}_{\text{kompakt}} \}$ kompakt.
Sei $V \subset \mathbb{R}^n \times \mathbb{R}^N \times \mathbb{R}^{Nn}$ offen, und sei Lagrange Funktion $F \in C^1(V,\mathbb{R})$.
Sei $U:=\{ u \in X | 1-Graph(u) \subset V \}$ (um $F(x,u(x),Du(x))$ definieren zu können)

Definiere *Variationsintegral*
$$
\mathcal{F}: U \to \mathbb{R}, \mathcal{F}(u):=\int_{\Omega}F(x,u(x),Du(x))
$$

**Lemma 2.16:**
![[Lemma 2.16]]

**Berechnung der ersten Variation:**
Mit dem Satz von der dominierten Konvergenz (glatt genug, beschränktes Gebiet) gilt:
$$
\begin{align}
\delta \mathcal{F}(u_{0},\xi)&=\frac{\mathrm{d}}{\mathrm{d}\varepsilon}\mathcal{F}(u_{0}+\varepsilon\xi) |_{\varepsilon=0} \\
&= \frac{\mathrm{d}}{\mathrm{d}\varepsilon}\int_{\Omega}F(x,u_{0}+\varepsilon \xi,Du_{0}+\varepsilon D\xi)dx|_{\varepsilon=0} \\
&= \int_{\Omega} \sum_{i=1}^N \frac{\partial F}{\partial z_{i}}(x,u_{0},Du_{0})\xi_{i}+\sum_{i=1}^N \sum_{j=1}^n \frac{\partial F}{\partial p_{ij}}(x,u_{0},Du_{0}) \frac{\partial \xi_{i}}{\partial x_{j}}dx   
\end{align}
$$
also ist $\delta \mathcal{F}(u_{0},\xi)$ ein bezüglich $\xi$ lineares Funktional $X$.

**Beispiel 2.17:**
![[Beispiel 2.17]]

**Anwendung:**
Sei $u(x)$ ein Potential, dann ist $-\nabla u$ ein Kraftfeld und der Integrand die Energiedichte dieses Kraftfelds.
$\mathcal{F}(u)$ ist dann die totale potentielle Energie des Potentials/Kraftfelds.
Physikalische Kraftfelder minimieren die darin gespeicherte Energie, also $\mathcal{F}(u)\to \mathrm{min}$.

**Beispiel 2.18:**
![[Beispiel 2.18]]

**Definition 2.19:**
![[Definition 2.19]]

Hierbei nimmt man $C$ mit rein wegen der Randbedingungen.

**Typische Beispiele für C:**
- $C=U$: keine Einschränkung, natürliche Randbedingung für $u$.
- $C= \{ u \in U | u(x)=g(x) \forall x \in \partial \Omega \}$: Dirichlet-Randbedingung.
- $C=\left\{  u \in U |\frac{\partial u}{\partial \nu}(x)=g(x) \forall x \in \partial \Omega \right\}$: Neumann-Randbedingung.

**Bemerkung 2.20:**
![[Bemerkung 2.20]]

**Lemma 2.21:**
![[Lemma 2.21]]

**Bemerkung 2.22:**
![[Bemerkung 2.22]]

**Satz 2.23:**
![[Satz 2.23]]

**Lemma 2.24:**
![[Lemma 2.24 (Fundamentallemma)]]

**Bemerkung 2.25:**
![[Bemerkung 2.25]]

**Zusammenfassung:**
Sei $F\in C^1, u \in C \subset U \subset X=C^1(\bar{\Omega},\mathbb{R}^N)$, und seien 
$$
Z(u,C):=\{ \xi \in X| \exists \varepsilon_{0} >0:\forall|\varepsilon|<\varepsilon_{0}: u+\varepsilon \xi \in C \}
$$
die zulässigen "Variationsrichtungen".
Bisher haben wir gezeigt:
Wenn $C_{0}^\infty(\Omega;\mathbb{R}^N)\subset Z(u,C)$ und $u$ schwache Minimalstelle von $\mathcal{F}$ in $C$ ist, dann löst $u$
zum einen die **schwache Form der EL-Gl:**
$$
\int_{\Omega}\sum_{i=1}^N\frac{\partial F}{\partial z_{i}}(x,u(x),Du(x))\xi_{i}(x)+\sum_{i=1}^N \sum_{j=1}^n \frac{\partial F}{\partial p_{ij}}(x,u(x),Du(x))\frac{\partial \xi_{i}}{\partial x_{j}}(x)dx=0 \forall \xi \in C_{0}^\infty(\Omega; \mathbb{R}^N).  
$$
und falls zusätzlich $\frac{\partial F}{\partial p_{ij}} \in C^1, u \in C^2(\Omega;\mathbb{R}^N)$ löst $u$ auch die **starke Form der EL-Gl.**:
$$L_{F}u=0$$
mit dem Euler-Operator $L_{F}:C^s(\Omega; \mathbb{R}^N)\to C^{s-2}(\Omega;\mathbb{R}^N), s\geq 2$.
$$
(L_{F}u)_{i}(x)= \frac{\partial F}{\partial z_{i}} (x, u(x), Du(x))- \sum_{j=1}^n \frac{\partial}{\partial x_{j}}\left[  \frac{\partial F}{\partial p_{ij}}(x,u(x),Du(x))  \right] ; \quad i=1,\dots,N.
$$
**Bemerkung 2.26:**
![[Bemerkung 2.26]]

**Beispiel 2.27:**
![[Beispiel 2.27]]

**Beispiel 2.28:**
![[Beispiel 2.28]]

**Beispiel 2.29:**
![[Beispiel 2.29]]
