$(x_1, x_2, u(x_1, x_2)), x = (x_1, x_2) \in \Omega$ sei eine Fläche im $\mathbb{R}^3$.

Oberfläche $= O(u) = \int_{\Omega} \sqrt{ 1+|\nabla u|^2 }\mathrm{d}x$.

**Aufgabe:** Finde Fläche minimalen Inhalts, die die Randbedingung $u = g$ auf $\partial \Omega$ erfüllt (→ *Variationsproblem*, d.h. Minimierung des Funktionals $O(u)$). 

**Anwendung:** eingespannte Membran, Seifenblasen 

Man kann zeigen (Integralsätze): $u(x)$ erfüllt die Minimalflächengleichung (quasilinear, glm. elliptisch) 
$$
\begin{cases}
\mathrm{div} \frac{\nabla u}{\sqrt{ 1+|\nabla u|^2 }} = 0 \text{ in } \Omega,\\
u = g \text{ auf } \partial \Omega.
\end{cases}
$$
, die hochgradig nichtlinear ist und außer in Trivialfällen ($g=C$) nicht analytisch lösbar ist, bzw: 

$(1 + u^2_{x_{2}})u_{x_{1}x_{1}} − 2u_{x_{1}} u_{x_{2}} u_{x_{1}x_{2}} + (1 + u_{x_{1}}^2 )u_{x_{2}x_{2}} = 0$.

Die ist quasilinear (kubisch nichtlinear) und glm. elliptisch in $x$ mit Koeffizientenmatrix:  $A = \begin{pmatrix} 1+u_{x_{2}}^2 & -u_{x_{1}}u_{x_{2}}\\ -u_{x_{1}}u_{x_{2}}& 1+u_{x_{2}}\end{pmatrix} \geq \mathrm{I}$.

Dabei ist $\kappa(x):=\frac{1}{2}\mathrm{div}(\frac{\nabla u}{\sqrt{ 1+|\nabla u|^2}})$ die *mittlere Krümmung der Fläche* (=Durchschnitt der Hauptkrümmungen d.h. Min./Max. der Normalkrümmungen). 
![[Pasted image 20260302145920.png]]
![[Pasted image 20260302145952.png]]
Rotiert man in der Richtung um den Winkel $\theta$ und ist die Fläche glatt, erhält man eine $\pi$-periodische, stetige Funktion $\tilde{\kappa}(\theta)$.
Diese hat ein Maximum/Minimum, die Extrema nennen wir *Hauptkrümmungen*
$\kappa(x)$ bezeichnet den Durchschnitt der beiden Hauptkrümmungen.


Geht die Kurve nach oben, einigen wir uns auf positvies Vorzeichen.
Geht die Kurve nach unten, einigen wir uns auf negatives Vorzeichen.

D.h. bei Minimalflächen muss die mittlere Krümmung für alle $x$ $0$ sein. Das bedeutet:
- wenn es in eine Richtung hinunter geht, muss es in der orthogonalen Richtung wieder rauf gehen und umgekehrt.
- Sattelform

Wenn die RB hinreichend "brav" ist, gibt es eine eindeutige Lösung.
