Der erste Piola-Kirchhoff Spannungstensor $T(x)=\mathrm{det}(\nabla \Phi(x))T^\Phi(x^\Phi)\nabla \Phi(x)^{-T}$ erfüllt die folgenden Gleichungen in der Referenzkonfiguration $\bar{\Omega}$:
1. $\forall x \in \Omega:-\mathrm{div}T(x)=f(x)$
2. $\forall x \in \Omega:\nabla \Phi(x)T(x)^T=T(x)\nabla \Phi(x)^T$
3. $\forall x \in \Gamma_{1}:T(x)n=g(x)$
wobei $f \mathrm{dx}=f^\Phi \mathrm{d}x^\Phi,g\mathrm{d}a=g^\Phi \mathrm{d}a^\Phi$.
Die erste und dritte Gleichung sind zusammen äquivalent zur variationellen Formulierung
$$
\int_{\Omega}T:\nabla \theta \mathrm{d}x=\int_{\Omega}f\cdot \theta \mathrm{d}x+\int_{\Gamma_{1}}g \cdot \theta \mathrm{d}a
$$
Für alle Vektorfelder $\theta:\bar{\Omega}\to \mathbb{R}^3$, die glatt genug sind und auf $\Gamma_{0}:=\Gamma-\Gamma_{1}$ folgende Gleichung erfüllen:
$$
\theta=0
$$
#### Beweis:
Die erste Gleichung folgt aus [[The Piola-Kirchhoff Stress Tensors#Erster Piola-Kirchhoff Spannungstensor]] und [[The Equations of Equilibrium and the Principle of Virtual Work in the Reference Configuration#Körperkräfte pro Einheitsvolumen]].

Die zweite erfolgt durch Nachrechnen.

Die dritte Gleichung folgt analog aus [[The Piola-Kirchhoff Stress Tensors#Erster Piola-Kirchhoff Spannungsvektor]] und [[The Equations of Equilibrium and the Principle of Virtual Work in the Reference Configuration#Oberflächenkräfte]].

Die Äquivalenz zur variationellen Formulierung zeigt man wie in [[Satz 2.4.1]].