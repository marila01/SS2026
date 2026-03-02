$(x_1, x_2, u(x_1, x_2)), x = (x_1, x_2) \in \Omega$ sei eine Fläche im $\mathbb{R}^3$.

Oberfläche $= O(u) = \int_{\Omega} \sqrt{ 1+|\nabla u|^2 }\mathrm{d}x$.

**Aufgabe:** Finde Fläche minimalen Inhalts, die die Randbedingung $u = g$ auf $\partial \Omega$ erfüllt (→ *Variationsproblem*, d.h. Minimierung des Funktionals $O(u)$). 

**Anwendung:** eingespannte Membran, Seifenblasen 

Man kann zeigen: $u(x)$ erfüllt die Minimalflächengleichung (quasilinear, glm. elliptisch) 
$$
\begin{cases}
\mathrm{div} \frac{\nabla u}{\sqrt{ 1+|\nabla u|^2 }} = 0 \text{ in } \Omega,\\
u = g \text{ auf } \partial \Omega.
\end{cases}
$$
bzw: 

$(1 + u^2_{x_{2}})u_{x_{1}x_{1}} − 2u_{x_{1}} u_{x_{2}} u_{x_{1}x_{2}} + (1 + u_{x_{1}}^2 )u_{x_{2}x_{2}} = 0$.

Koeffizientenmatrix:  $A = \begin{pmatrix} 1+u_{x_{2}}^2 & -u_{x_{1}}u_{x_{2}}\\ -u_{x_{1}}u_{x_{2}}& 1+u_{x_{2}}\end{pmatrix} \geq \mathrm{I}$.

Dabei ist $\frac{1}{2}\mathrm{div}(\frac{\nabla u}{\sqrt{ 1+|\nabla u|^2}})$ die *mittlere Krümmung der Fläche* (=Durchschnitt der Hauptkrümmungen d.h. Min./Max. der Normalkrümmungen). 

**Minimalflächen:** mittlere Krümmung $≡ 0 ⇒$ lokale Sattelform.