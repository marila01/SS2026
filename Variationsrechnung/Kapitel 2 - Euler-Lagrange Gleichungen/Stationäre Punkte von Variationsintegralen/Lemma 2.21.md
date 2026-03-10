Sei $u$ schwache Minimalstell von $\mathcal{F}$ in einer Menge $C \subset U \subset X$, und sei $u+ \xi \in C \quad \forall \xi \in C_{0}^\infty(\Omega;\mathbb{R}^N)$.
$$
\delta \mathcal{F}(u,\xi)=0 \quad \forall \xi \in C_{0}^\infty(\Omega; \mathbb{R}^N)
$$
##### Beweis:
Laut [[Definition 2.19]] existiert $\delta_{0}>0$ mit $\mathcal{F}(u)\leq \mathcal{F}(v)$ $\forall v \in C\cap B_{\delta_{0}}(u;X)$.
Sei $\xi \in C_{0}^\infty(\Omega; \mathbb{R}^N)\implies u+\xi \in C$ und $\exists \delta_{1}>0$ mit $||\delta_{1}\xi||_{X}<\delta_{0}$
$$
\implies \phi(0)=\mathcal{F}(u)\leq \mathcal{F}(u+\varepsilon \xi)=\phi(\varepsilon) \text{ für } |\varepsilon|<\delta_{1}.
$$
$$
\implies \phi'(0)=\delta \mathcal{F}(u,\xi)=0
$$
Dass die erste Variation überhaupt erst existiert, folgt aus [[Lemma 2.16]].
