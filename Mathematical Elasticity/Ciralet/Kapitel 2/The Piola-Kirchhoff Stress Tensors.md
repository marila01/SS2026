Wir wollen schlussendlich das Deformationsfeld und den Cauchy stress tensor unseres Körpers unter gegebener Krafteinwirkung bestimmen.
Damit sind aber unsere Gleichgewichts-Gleichungen über der deformierten Konfiguration (vgl. [[Satz 2.3.1 von Cauchy- Der Cauchy'sche Spannungstensor]]) nicht so nützlich, da die in der **Euler-Variablen** $x^\Phi=\Phi(x)$ ausgedrückt sind (also unserer Unbekannten).
Wir müssen also das System umschreiben, sodass wir unser RWP in der **Lagrange-Variablen** $x$ stehen haben. Zusätzlich wäre es gut, wenn wir unsere Divergenzform behalten würden, da wir dadurch eine variationelle Formulierung erhalten.
Das macht man mit der **Piola-Transformation**:

#### Erster Piola-Kirchhoff Spannungstensor
$T:\bar{\Omega}\to \mathbb{M}^3$ heißt Piola-Transformation von $T^\Phi:\bar{\Omega}^\Phi\to \mathbb{M}^3$ Tensorfeld, wenn
$$
T(x)=(\mathrm{det}(\nabla \Phi(x)))T^\Phi(x^\Phi)\nabla \Phi(x)^{-T}, x^\Phi=\Phi(x)
$$
Wenden wir das auf den Cauchy stress tensor $T^\Phi$ an, nennt man $T$ den **ersten Piola-Kirchhoff Spannungstensor**.
Es gilt: $\mathrm{div}(T(x))=(\mathrm{det}(\nabla \Phi(x)))\mathrm{div}^\Phi(T^\Phi(x^\Phi)), x^\Phi=\Phi(x)$.

Man kann also die Gleichgewichtsgleichungen über der deformierten Konfiguration transformieren zu Gleichungen über der Referenzkonfiguration mit ähnlicher (Divergenz-)Struktur (siehe [[Satz 2.6.1]]).
Wie schon vorher erwähnt, gibt es für das RWP eine variationelle Formulierung ([[Satz 2.4.1]]) und nach der Transformation gibt es auch eine über der Referenzkonfiguration ([[Satz 2.6.1]]).

#### Erster Piola-Kirchhoff Spannungsvektor
Man kann auch den Cauchy stress vector $t^\Phi(x^\Phi,n^\Phi)$ derartig transformieren, dass $t(x,n)=T(x)n$:
Da $T(x)n\mathrm{d}a=T^\Phi(x^\Phi)n^\Phi\mathrm{d}a^\Phi$ (aus Satz 1.7.1) kann man durch $t^\Phi(x^\Phi,n^\Phi)\mathrm{d}a^\Phi=t(x,n)\mathrm{d}a$ $t$ definieren und es folgt die Behauptung.
$t(x,n)$ heißt **first Piola-Kirchhoff stress vector** am Punkt $x\in \bar{\Omega}$ über einem orientierten Flächenelement mit Normalvektor $n$.
$t:\bar{\Omega}\times S_{1}\to \mathbb{R}^3$ misst also die Dichte der Oberflächenkräfte pro Flächenelement in der Referenzkonfiguration.

$T(x)$ ist im Allgemeinen nicht symmetrisch, aber die konstituitiven Gleichungen aus Kapitel 3 würden sich vereinfachen, wenn er das wäre.

#### Zweiter Piola-Kirchhoff Spannungstensor
Daher definieren wir den **zweiten Piola-Kirchhoff'schen Spannungstensor** $\Sigma(x)$ durch
$$
\Sigma(x)=\nabla \Phi(x)^{-1}T(x)=\mathrm{det}(\nabla \Phi(x))\nabla \Phi(x)^{-1}T^\Phi(x^\Phi)\nabla \Phi(x)^{-T}, x^\Phi=\Phi(x).
$$
$T(x)$ und $\Sigma(x)$ hängen beide von $\Phi$ ab, zum einen wegen der Transformation und zum anderen, weil der Cauchy stress tensor auch von $\Phi$ abhängt, diese Abhängigkeiten betrachtet man genauer in Kapitel 3.