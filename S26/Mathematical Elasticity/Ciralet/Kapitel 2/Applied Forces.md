Wir betrachten 2 Arten von Kräften, die auf den deformierten Körper $\bar{\Omega}^\Phi$ wirken:
#### Angewandte Körperkräfte (applied bodyforces in the deformed configuration)
- Durch Vektorfeld $f^\Phi:\Omega^\Phi \to \mathbb{R}^3$ definiert.
- $f^\Phi$ heißt Dichte der angewandten Körperkräfte pro Einheitsvolumen in der deformierten Konfiguration.
- Sei $\rho ^\Phi : \Omega^\Phi \to \mathbb{R}$ Massendichte in der deformierten Konfiguration, d.h. die Masse einer $\mathrm{d}x^\Phi$ Teilmenge $A^\Phi \subset \bar{\Omega}^\Phi$ ist gegeben durch  $\int_{A^\Phi}\rho^\Phi(x^\Phi)\mathrm{d}x^\Phi$, wir nehmen weiters an $\forall x^\Phi \in \Omega^\Phi:\rho^\Phi(x^\Phi)>0$. Dann kann man äquivalent schreiben als $f^\Phi=\rho^\Phi b^\Phi$, wobei man $b^\Phi:\Omega^\Phi \to \mathbb{R}^3$ die Dichte pro Einheitsmasse in der deformierten Konfiguration nennt.
- Für $x^\Phi \in \Omega^\Phi$ beschreibt $f(x^\Phi)\mathrm{d}x^\Phi$ die Kraft, die auf das Volumenelement $\mathrm{d}x^\Phi$ wirkt.
- Beispiele dafür sind Gravitation oder elektrostatische Kräfte.
#### Angewandte Oberflächenkräfte (applied surface forces in the deformed configuration)
- Durch Vektorfeld $g^\Phi:\Gamma_{1}^\Phi \to \mathbb{R}^3$ definiert.
- Dichte auf $\mathrm{d}a^\Phi$- messbarer Teilmenge $\Gamma_{1}^\Phi \subset \partial \Omega^\Phi$.
- Dichte der angewandten Oberflächenkräfte pro Einheitsfläche in der deformierten Konfiguration.
- Für $x^\Phi \in \Gamma_{1}^\Phi$ beschreibt $g^\Phi(x^\Phi)\mathrm{d}a^\Phi$ die Kraft, die auf ein Flächenelement $\mathrm{d}a^\Phi$ wirkt.
- Meistens wirkt da ein ander Körper auf diesen Teil vom Rand [[Examples of Applied Forces; Conservative Forces]].
- Die Kräfte sind oft nicht überall spezifiziert, z.B. ist manchmal nur die Normalenkomponente $g^\Phi \cdot n^\Phi$ auf $\Gamma_{1}^\Phi$ bekannt. Anfangs beschränken wir uns auf überall bekanntes $g^\Phi$ auf $\Gamma_{1}^\Phi$ oder ganz unspezifierte Oberflächenkräfte.
- Falls man die Oberflächenkräfte gar nicht kennt, braucht man, damit das Problem well-posed ist, Kenntnis der actual Deformation auf $\Gamma_{0}:=\Phi^{-1}(\Gamma^\Phi-\Gamma^\Phi_{1})$.
