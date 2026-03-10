Sei $S:\bar{B_{1}} (0) \to \bar{B_{1}}(0)$ eine stetige Funktion, wobei $\bar{B_{1}}(0)$ die abgeschlosse Einheitskugel im $\mathbb{R}^n$ sei; dann existiert ein Fixpunkt von $S$.

Der Satz von Brouwer wird zum Beispiel in Evans 10, Sec. 8.1.4 bewiesen.

#### Beweis:
##### Schritt 1:
*Behauptung: Es gibt keine $C^1$- Funktion $w:\bar{B_{1}(0)}\to \partial B_{1}(0)$ sodass $w(x)=x$ auf $\partial B_{1}(0)$.*

Angenommen nicht: Dann gilt $w=id$ auf $\partial B_{1}(0)$.
Daraus folgt mittels partieller Integration
$$\int_{B_{1}(0)}\mathrm{det}\nabla w(x)dx=\int_{B_{1}(0)}\det \nabla id(x) dx=\int_{B_{1}(0)}1dx=\lambda(B_{1}(0))\neq 0$$
Aber $\forall x \in \bar{B_{1}(0)}:|w(x)|=1$, da $w(x)\in \partial B_{1}(0)$.
Also $|w(x)|^2=1$ auf $\bar{B_{1}(0)}$.
Ableiten liefert $2 (Dw)^Tw=0$, also ist $0$ ein Eigenwert von $Dw^T$ und damit $\det Dw^T_{0}=0$. Widerspruch.

##### Schritt 2:
*Gleiche Behauptung für Schritt 1 nur für $w$ stetig*.
Angenommen nicht: Dann könnten wir ein $\tilde{w}$ definieren mit
$$
\tilde{w}(x)=
\begin{cases}
w(x) \text{ für } x \in \bar{B_{1}(0)} \\
x \text{ für } x \in (\bar{B_{1}(0)})^C
\end{cases}
$$
stetig aber nicht $C^1$.
Wir haben $\forall x \in \mathbb{R}^n$: $\tilde{w}(x)\neq 0$.
Betrachte nun 
$$
w_{1}^\varepsilon(x):=(\eta_{\varepsilon} \ast \tilde{w})(x)\in C^1(\Omega),
$$
wobei $\eta_{\varepsilon}$ ein glatter, radialer Mollifyer ist.
Es gilt $w_{1}^\varepsilon(x)=x$ für $(\bar{B_{2}(0)})^C$ für kleine $\varepsilon$. (NACHRECHNEN!)
Definiere 
$$
w_{2}^\varepsilon(x):=2 \frac{w^\varepsilon_{1}(x)}{|w_{1}^\varepsilon(x)|}.
$$
Man kann zeigen, dass $w_{2}\in C^1(\mathbb{R}^n), |w_{2}^\varepsilon(x)|=2$ auf $\bar{B_{2}(0)}$. (NACHRECHNEN).
Dann ist $w_{2}^\varepsilon: \bar{B_{2}(0)}\to \partial B_{2}(0)$, $w_{2}^\varepsilon(x)=x$ auf $\partial B_{2}(0)$ und $w_{2}^\varepsilon \in C^1(\mathbb{R}^n)$. Das ist aber (mod Skalierung) lt. [[#Schritt 1]] nicht möglich. Widerspruch.

##### Schritt 3:
(Bissi handwavey)
Sei $S:\bar{B_{1}(0)}\to \bar{B_{1}(0)}$ stetig.
Angenommen, es gäbe keine Fixpunkte.
Dann kann man ein $w:\bar{B_{1}(0)}\to \partial B_{1}(0)$ konstruieren, indem man die Gerade zwischen $S(x)$ und $x$ bis zum Rand der Einheitskugel verlängert und diesen Punkt $w(x)$ nennt (wie in der Skizze), mit $w(x)=x$ auf $\partial B_{1}(0)$ und $w$ stetig.
Aus [[#Schritt 2]] folgt der Widerspruch.
