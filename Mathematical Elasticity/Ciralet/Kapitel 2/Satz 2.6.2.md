Direkt aus [[Satz 2.6.1]] erhält man:

Der zweite Piola-Kirchhoff stress tensor $\Sigma(x)=\mathrm{det}(\nabla \Phi(x))\nabla \Phi(x)^{-1}T^\Phi(x^\Phi)\nabla \Phi(x)^{-T}$ erfüllt in der Referenzkonfiguration $\bar{\Omega}$ folgende Gleichungen:
1. $\forall x \in \bar{\Omega}:-\mathrm{div}(\nabla \Phi(x)\Sigma(x))=f(x)$
2. $\forall x \in \Omega: \Sigma(x)=\Sigma(x)^T$
3. $\forall x \in \Gamma_{1}:\nabla \Phi(x)\Sigma(x)n=g(x)$
Die erste und dritte Gleichung zusammen sind äquivalent zu den variationellen Gleichungen
$$
\int_{\Omega}\nabla \Phi \Sigma:\nabla \theta \mathrm{d}x=\int_{\Omega}f \cdot \theta \mathrm{d}x+\int_{\Gamma_{1}}g \cdot \theta \mathrm{d}a
$$
	für alle Abbildungen $\theta:\bar{\Omega}\to \mathbb{R}^3$ glatt genug, für die auf $\Gamma_{0}$ gilt
	$$
	\theta=0
	$$ 