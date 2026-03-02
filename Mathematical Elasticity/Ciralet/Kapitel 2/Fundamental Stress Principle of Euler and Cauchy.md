In der Kontinuumsmechanik für statische Probleme gilt das folgende Axiom (stress principle of Cauchy and Euler).

Sei $\bar{\Omega}^\Phi$ die deformierte Konfiguration unseres Körpers, $f^\Phi:\Omega^\Phi \to \mathbb{R}^3$, $g^\Phi :\Gamma_{1}^\Phi\to \mathbb{R}^3$ die jeweiligen Kraftdichten.

Dann existiere ein Vektorfeld $t^\Phi:\bar{\Omega}^\Phi \times S_{1}\to \mathbb{R}^3$, sodass
- $\forall A^\Phi \subset \bar{\Omega}^\Phi, x^\Phi \in \Gamma_{1}^\Phi \cap \partial A^\Phi$, wo der äußere Normalenvektor $n^\Phi$ auf $\Gamma_{1}^\Phi \cap \partial A^\Phi$ existiert: $t^\Phi(x^\Phi,n^\phi)=g^\Phi(x^\Phi)$. ^3f1f65
- $\forall A^\Phi \subset \bar{\Omega}^\Phi:\int_{A^\Phi}f^\Phi(x^\Phi)\mathrm{d}x^\Phi+\int_{\mathrm{d}A^\Phi}t^\Phi(x^\Phi,n^\Phi)\mathrm{d}a^\Phi=0$, wobei $n^\Phi$ äußerer Einheitsnormalenvektor auf $\partial A^\Phi$ ist. (Axiom of force Balance)
- $\forall A^\Phi \subset \bar{\Omega}^\Phi:\int_{A^\Phi}\vec{o x^\Phi}\times f^\Phi(x^\Phi)\mathrm{d}x^\Phi+\int_{\partial A^\Phi}\vec{o x^\Phi}\times t^\Phi(x^\Phi,n^\Phi)\mathrm{d}a^\Phi=0$, wobei $o$ der Ursprung ist. (Axiom of moment balance)

Dieses Axiom sagt uns folgendes:
1. Es gibt elementare Oberflächenkräfte $t^\Phi(x^\Phi,n^\Phi)\mathrm{d}a^\Phi$ entlang der Ränder aller Teilstücke in der Referenzkonfiguration.
2. An einem Punkt $x^\Phi$ am Rand $\partial A^\Phi$ einer Teilmenge $A^\Phi$ hängt die elementare Oberflächenkraft nur über den Normalenvektor $n^\Phi$ von $A^\Phi$ ab und nicht einmal von irgendwelchen geometrischen Eigenschaften wie z.B. Krümmung oder so.
3. Jede Teilmenge $A^\Phi \subset \bar{\Omega}^\Phi$ (Auch $\bar{\Omega}^\Phi$ selber) ist in einem statischen Gleichgewicht insofern, dass der Torsor zwischen $t^\Phi(x^\Phi,n^\Phi)$ und $f^\Phi(x^\Phi)\mathrm{d}a^\Phi$ äquivalent zu 0 ist, d.h. die Resultante verschwindet (axiom of force balance) und das resultierende Moment bzgl. des Ursprungs $o$ auch (axiom of moment balance).

Intuitiv heißt das, dass das statische Gleichgewicht jeder Teilmenge $A^\Phi \subset \bar{\Omega}^\Phi$ durch den Effekt elementarer Oberflächenkräfte dieser Form auf den Rand $\partial A^\Phi$ möglich gemacht wird.
Schneidet man also (gedanklich) den Körper beliebig auseinander, wirken Kontaktkräfte auf die Stücke, die man durch eine elementare Oberflächenkraft an den (gedachten) Schnittflächen ($t^\Phi$) ausdrücken kann.

Für jeden Punkt $x^\Phi \in \bar{\Omega}^\Phi$ heißt $t^\Phi(x^\Phi,n^\Phi)$ der Cauchy-Spannungsvektor (Cauchy stress vector).
 