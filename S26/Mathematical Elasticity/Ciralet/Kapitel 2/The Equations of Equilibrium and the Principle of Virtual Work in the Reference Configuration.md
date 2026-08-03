Man muss nach [[The Piola-Kirchhoff Stress Tensors]] also nur mehr die Kraftdichten transformieren:
#### Körperkräfte pro Einheitsvolumen
Wir betrachten also ein Vektorfeld $f:\Omega \to \mathbb{R}^3$ sodass
$$
\forall x^\Phi=\Phi(x)\in \Omega ^\Phi:f(x)\mathrm{d}x=f^\Phi(x^\Phi)\mathrm{d}x
$$
Da $\mathrm{d}x^\Phi=\mathrm{det}(\nabla \Phi)\mathrm{d}x$:
$$
\forall x^\Phi=\Phi(x)\in \Omega^\Phi:f(x)=\mathrm{det}(\nabla \Phi(x))f^\Phi(x^\Phi)
$$
Den Vorfaktor kennen wir schon von den Divergenzen der Tensoren und werden diese Zusammenhang in [[Satz 2.6.1]] verwenden.
Das Vektorfeld $f$ misst die *Dichte der angewandten Körperkräfte pro Einheitsvolumen in der Referenzkonfiguration*.

#### Massendichte, Körperkräfte pro Einheitsmasse
Sei $\rho:\Omega\to \mathbb{R}$ die Massendichte der Referenzkonfiguration. Aus denselben Gründen wie oben gilt:
$$
\forall x^\Phi=\Phi(x)\in \Omega ^\Phi: \rho(x)=\mathrm{det}(\nabla \Phi(x))\rho ^\Phi(x^\Phi)
$$
Diese Gleichung belegt (unabhängig zur Definition einer Deformation, in der genau das verlangt wird), dass $\mathrm{det}(\nabla \Phi)>0$, da die Massendichte (zumindest makroskopisch) immer positiv sein muss.

Definieren wir nun die *Dichte der Körperkraft pro Einheitsmasse in der Referenzkonfiguration* $b:\Omega\to \mathbb{R}^3$ mit $f=\rho b$ folgt:
$$
\forall x^\Phi=\Phi(x)\in \Omega ^\Phi:b(x)=b^\Phi(x^\Phi)
$$
#### Oberflächenkräfte
Nun wollen wir die Randbeding $T^\Phi n^\Phi=g^\Phi$ über einem Teil des Randes $\Gamma_{1}^\Phi=\Phi(\Gamma_{1})$ deformierten Konfiguration transformieren, und zwar in eine ähnliche über $\Gamma_{1}$.
Dafür verwenden wir den ersten Piola-Kirchhoff stress vector aus [[The Piola-Kirchhoff Stress Tensors#Erster Piola-Kirchhoff Spannungsvektor]].
Wir definieren $g: \Gamma_{1}\to \mathbb{R}^3$ durch $\forall x^\Phi=\Phi(x)\in \Gamma_{1}:g(x)\mathrm{d}a=g^\Phi(x^\Phi)\mathrm{d}a^\Phi$ und erhalten aus Satz 1.7-1:
$$
g(x)=\mathrm{det}(\nabla \Phi(x))||\nabla \Phi(x)^{-T}n||g^\Phi(x^\Phi).
$$
Man bemerke, dass $g(x)$ sowohl durch die Definition über die Flächenelemente als auch über $g^\Phi$ von $\Phi$ abhängt.
Das Vektorfeld $g:\Gamma_{1}\to \mathbb{R}^3$ misst die *Dichte der Oberflächenkraft pro Flächenelement in der Referenzkonfiguration*.


Es gibt ein Analogon zu [[Satz 2.4.1]] über der Referenzkonfiguration, nämlich [[Satz 2.6.1]].
Transformiert man auf den [[The Piola-Kirchhoff Stress Tensors#Zweiter Piola-Kirchhoff Spannungstensor]], erhält man durch [[Satz 2.6.2]] außerdem äquivalente Gleichgewichtsgleichungen.

Diese Gleichungen nennt man *equations of equilibrium in the reference configuration* und die variationellen Gleichungen nennt man *principle of virtual wok om the reference condition*.
Die Gleichung über $\Gamma_{1}$ nennt man auch *boundary condition of traction*

Später hängen wir noch eine *boundary condition of place* in Form von $\Phi=\Phi_{0}$ auf $\Gamma_{0}$ an, mit $\Phi_{0}:\Gamma_{0}\to \mathbb{R}^3$ gegeben.
Arbeiten wir unter diesen Rahmenbedingung, kann man jedes Vektorfeld $\theta:\bar{\Omega}\to \mathbb{R}^3$ im principle of virtual work als eine *"virtuelle" Variation einer Deformation konsistent mit den boundary conditions of place* auffassen.
Definieren wir die Menge 
$$
\varphi:= \{ \psi:\bar{\Omega}\to \mathbb{R}^3; \mathrm{det}(\nabla \psi)>0 \text{ in } \bar{\Omega}; \psi=\Phi_{0} \text{ auf } \Gamma_{0} \}
$$
(Später fordern wir auch noch die Injektivität der Menge- siehe Kapitel 5)
Wir bemerken, dass der Tangentialraum $T_\vartheta$ an einem Punkt $\vartheta$ auf der Mannigfaltigkeit $\varphi$ genau so aussieht:
$$
T_{\vartheta}\varphi:=\{ \theta:\bar{\Omega}\to \mathbb{R}^3; \theta=0 \text{ auf }\Gamma_{0} \}
$$
Daher kann man die Vektorfelder aus dem Tangentialraum auch als Variationen verstehen.

Das Attribut "virtuell" kommt davon, dass diese Objekte keine physikalische Interpretation besitzen (müssen).

#### Bemerkungen
1. Genaueres dazu in Kapitel 4 und 5, wo es um stationäre Funktioale in der Variationsrechnung geht.
2. Den Tangentialraum einzuführen, macht sehr viel Sinn, wenn man z.b. zusätzlich noch constraints für zulässige Deformationen (zb incompressability) festlegt.
3. Die Regulartitäten bei den Kraftdichten kann man abschwächen.
