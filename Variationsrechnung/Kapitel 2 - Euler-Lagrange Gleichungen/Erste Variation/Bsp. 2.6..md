Sei 
$$
\mathcal{F}(u):=\int_{0}^{b_{1}}\sqrt{ \frac{1+u'(x)^2}{x} }dx \quad \text{auf } U:=\{ u \in C^1[0,b_{1}] \text{ }| \text{ }u(0)=0, u(b_{1})=b_{2} \}
$$
(vgl. [[Bsp. 1.3. Brachistochrone]])

$$
\{ u_{0}+\varepsilon \xi \text{ }|\text{ } |\varepsilon|<\varepsilon_{0} \}\subset U \iff \xi \in \tilde{U}:=\{\eta \in C^1[0,b_{1}] \text{ } |\text{ } \eta(0)=\eta(b_{1})=0 \}.
$$
Für $\xi \in \tilde{U}$ gilt
$$
\phi(\varepsilon)=\mathcal{F}(u_{0}+\varepsilon \xi)=\int_{0}^{b_{1}}\sqrt{ \frac{(1+(u_{0}'+\varepsilon \xi'))^2}{x} }dx.
$$
Mit dem Satz von der dominierten Konvergenz (von Lebesgue) gilt:
$$
\delta \mathcal{F}(u_{0},\xi)=\phi'(0)=\int_{0}^{b_{1}} \frac{\partial}{\partial\varepsilon} \sqrt{ \frac{(1+(u_{0}'+\varepsilon \xi'))^2}{x} }_{|\varepsilon=0}dx=\int_{0}^{b_{1}}\frac{u_{0}'(x)}{\sqrt{ x(1+u_{0}'(x)^2) }} \xi'(x)dx \quad \text{existiert.}
$$
**Berechnung der Brachistochrone:**
Sei $u_{0}$ eine Minimalstelle von $\mathcal{F}$.

*Annahme:* $y \in C[0,b_{1}]$. (Eine sauberere aber technischere Herleitung ist in [GH]§6.2.3.)

Wähle speziell
$$
\xi(x):=\int_{0}^x y(\tau)d\tau-Cx, \quad C=\frac{1}{b_{1}}\int_{0}^{b_{1}}y(x)dx \quad \implies \xi \in \tilde{U}.
$$

Dann folgt wegen [[Bem. 2.3.]] 
$$
0=\delta \mathcal{F}(u_{0},\xi)=\int_{0}^{b_{1}}y(x)(y(x)-C)dx=\int_{0}^{b_{1}}y(x)^2-2Cy(x)+C^2dx=\int_{0}^{b_{1}}(y(x)-C)^2dx,
$$
da $\int_{0}^{b_{1}}Cy(x)dx=b_{1}C^2=\int_{0}^{b_{1}}C^2dx.$

$$
\implies y(x)=C, \text{ also aus } C[0,b_{1}]\implies u_{0}'=\sqrt{ \frac{x}{D-x} } \text{ für ein }D>b_{1}\\
$$
$$
\implies u_{0}(x)=D\cdot \mathrm{arctan}\sqrt{ \frac{x}{D-x} }-\sqrt{ Dx-x^2 } \text{ (da } u_{0}=0; \text{ Zykloide),}
$$
$D$ kann eindeutig so gewählt werden, dass $u_{0}(b_{1})=b_{2}$.
