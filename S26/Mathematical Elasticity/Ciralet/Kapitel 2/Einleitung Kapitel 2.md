Im Gegensatz zur formalen Rechnung im ModPDEs-Skript, wählt Ciralet einen Zugang über die deformierte Konfiguration $\bar{\Omega}^\Phi$ und liefert rigoros die nötigen Gleichungen.

Unser Körper ist im statischen Gleichgewicht, wenn das [[Fundamental Stress Principle of Euler and Cauchy]] ist.

Dieses Axiom impliziert schließlich den [[Satz 2.3.1 von Cauchy- Der Cauchy'sche Spannungstensor]].
Dieser besagt, dass es ein symmetrisches Tensofeld $T^\Phi:\bar{\Omega}^\Phi\to \mathbb{S}^3$ gibt, sodass
$$
\begin{cases} -\mathrm{div}^\Phi(T^\Phi)=f^\Phi \text{ in } \Omega^\Phi \\
T^\Phi \cdot n^\Phi=g^\Phi \text{ auf } \Gamma_{1}^\Phi

\end{cases}
$$
wobei $n^\Phi$ den Äußeren Einheitsnormalenvektor auf $\Gamma_{1}^\Phi$ beschreibt.
Man nennt diese Gleichungen auch die *equilibrium equations over the deformed configuration*.
$T^\Phi$ nennt man auch den Cauchy-Spannungstensor (cauchy stress tensor).

Diese Formulierung hat den Vorteil, dass sie Divergenzstruktur hat. 
Jedoch hat sie den Nachteil, dass sie in $\Phi$ ausgedrückt wird, welches wir nicht kennen.

Eine Möglichkeit, um die Divergenzstruktur beizubehalten und gleichzeitig Gleichungen über die Referenzkonfiguration zu erhalten, ist die Piola-Transformation des Cauchy-Spannungstensorfelds, $T:\bar{\Omega}\to \mathbb{M}^3, T(x):=T^\Phi(x^\Phi)\mathrm{Cof}(\nabla \Phi(x))$.

Man kann dann zeigen ([[Satz 2.6.1]]), dass die *equilibrium equations over the deformed configuration* äquivalent zu den transformierten *equilibrium equations over the reference configuration $\bar{\Omega}$* sind , mit
$$
\begin{cases}
-\mathrm{div}(T)=f \text{ in } \Omega
 \\
T \cdot n = g \text{ auf } \Gamma_{1} 
\end{cases}
$$
mit $n$ äußerer Einheitsnormalenvektor auf $\Gamma_{1}$, $f,g$ sodass $f \mathrm{d}x=f^\Phi \mathrm{d}x^\Phi$, $g \mathrm{d}a=g^\Phi \mathrm{d}a^\Phi$.
Da wir immer noch in Divergenzform sind, gibt es eine variationelle Formulierung ([[Satz 2.6.1]]), die man *principle of virtual work* nennt (vgl. [[Welche Gleichungen betrachtet man]]).
In Kapitel 4 spielt diese Formulierung eine große Rolle in der Theorie hyperelastischer Materialien.

$T$ nennt man ersten Piola-Kirchoff Spannungstensor.
Außerdem gibt es den symmetrischen Piola-Kirchhoff Spannungstensor $\Sigma:= \nabla \Phi^{-1}T$, den wir schon aus [[Welche Gleichungen betrachtet man]] kennen.
[[Satz 2.6.2]] liefert den Zusammenhang zum ModPDEs Skript.

Der kommt wieder, wenn man die constituitiven Gleichungen (also die materialabhängigen) von elastischen Materialien betrachtet (Kapitel 3).

Schlussendlich werden mehrere Beispiele für Kräfte und Kraftdichten $f$ und $g$ beschrieben.

