Das Randwerdproblem
1. $-\mathrm{div}^\Phi T^\Phi=f^\Phi \text{ auf }\Omega^\Phi$
2. $T^\Phi n^\Phi=g^\Phi \text{ auf } \Gamma_{1}^\Phi$
ist formal äquivalent zu den variationellen Gleichungen
$$
\int_{\Omega^\Phi}T^\Phi:\nabla ^\Phi \theta^\Phi
\mathrm{d}x^\Phi=\int_{\Omega ^\Phi}f^\Phi \cdot \theta ^\Phi \mathrm{d}x ^\Phi+\int_{\Gamma_{1}}g^\Phi \cdot \theta ^\Phi \mathrm{d}a^\Phi$$
für $\theta^\Phi:\Omega^\Phi\to \mathbb{R}^3$glatt genug mit mit
$$
\theta^\Phi=0 \text{ auf } \Gamma_{0}^\Phi:=\Gamma^\Phi-\Gamma_{1}^\Phi.
$$
#### Beweis
Wir wenden wieder eine Green'sche Formel an:
Für jedes Tensorfeld $T^\Phi:\bar{\Omega}^\Phi\to\mathbb{M}^3$ und Vektorfeld $\theta^\Phi:\bar{\Omega}^\Phi\to \mathbb{R}^3$ gilt
$$
\int_{\Omega^\Phi}\mathrm{div}^\Phi T^\Phi \cdot \theta^\Phi \mathrm{d}x^\Phi=-\int_{\Omega^\Phi}T^\Phi:\nabla^\Phi \theta^\Phi
\mathrm{d}x^\Phi+\int_{\Gamma^\Phi}T^\Phi n^\Phi \cdot \theta^\Phi \mathrm{d}a^\Phi.$$
Da Gleichungen 1 und 2 gelten und $\theta$ so gewählt ist, dass es außerhalb von $\Gamma_{1}^\Phi$ verschwindet, erhalten wir
$$
\begin{align} 0 &=\int_{\Omega^\Phi}(\mathrm{div}^\Phi T^\Phi+f^\Phi) \cdot \theta^\Phi \mathrm{d}x^\Phi  \\
 &= \int_{\Omega^\Phi}[-T^\Phi:\nabla ^\Phi \theta^\Phi
+f^\Phi \cdot \theta ^\Phi] \mathrm{d}x ^\Phi+\int_{\Gamma_{1}}T^\Phi n^\Phi \cdot \theta ^\Phi \mathrm{d}a^\Phi \\
&= \int_{\Omega^\Phi}[-T^\Phi:\nabla ^\Phi \theta^\Phi
+f^\Phi \cdot \theta ^\Phi] \mathrm{d}x ^\Phi+\int_{\Gamma_{1}}g^\Phi \cdot \theta ^\Phi \mathrm{d}a^\Phi

\end{align}
$$

Umgekehrt, falls die variationellen Gleichungen erfüllt sind und $\theta ^\Phi=0$ auf $\Gamma^\Phi$, gilt
$$
\int_{\Omega^\Phi}T^\Phi:\nabla ^\Phi \theta^\Phi
\mathrm{d}x^\Phi=\int_{\Omega ^\Phi}f^\Phi \cdot \theta ^\Phi \mathrm{d}x 
$$
und wegen obiger Green'scher Formel
$$
\int_{\Omega^\Phi}T^\Phi:\nabla ^\Phi \theta^\Phi
\mathrm{d}x^\Phi=-\int_{\Omega^\Phi}\mathrm{div}^\Phi T^\Phi \cdot \theta^\Phi \mathrm{d}x^\Phi
$$
Daraus folgt $\mathrm{div}^\Phi T^\Phi+f^\Phi=0$ auf $\Omega ^\Phi$.
Nun setzen wir diese Gleichung wieder in die Green'sche Formel ein und erhalten
$$
\int_{\Gamma_{1}^\Phi}T^\Phi n^\Phi \cdot \theta ^\Phi \mathrm{d}a^\Phi=\int_{\Gamma_{1}^\Phi}g^\Phi \cdot \theta ^\Phi \mathrm{d}a^\Phi,
$$
also $T^\Phi n^\Phi=g^\Phi$ auf $\Gamma_{1}^\Phi$.
