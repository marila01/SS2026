---
aliases:
  - "Theorem 1.4.: Einbettungssatz von Sobolev"
---
Seien $\Omega \in \mathbb{R}^n$ ein beschränktes Gebiet mit $\partial \Omega \in C^1$ ($C^{0,1}$ genügt.) und $1\leq p,q<\infty$, $k,m \in \mathbb{N}_{0}$ mit $m>k$.
1. Die Einbettung $W^{m,p}(\Omega) \hookrightarrow W^{k,q}(\Omega)$ ist stetig, wenn $m-\frac{n}{p}\geq k-\frac{n}{q}$ und kompakt, wenn $m-\frac{n}{p}> k-\frac{n}{q}$.
2. Die Einbettung $W^{m,p}(\Omega) \hookrightarrow C^k(\bar{\Omega})$ ist kompakt, wenn $m-\frac{n}{p}>k$. 
Für beliebige beschränkte Gebiete gelten beide Aussagen für $W_{0}^{m,p}(\Omega)$ anstatt $W^{m,p}(\Omega)$.

Um Einbettungen $H^1(\Omega)\hookrightarrow L^p(\Omega)$ kompakt formulieren zu können, führen wir die folgende Notation ein.
Seien die Intervalle
$$
N^*=\begin{cases} \left[1, \frac{2n}{n-2} \right] \text{ für }n\geq 3,\\
[1,+\infty) \text{ für } n=2, \\
[1,+\infty] \text{ für }n=1
\end{cases}
$$
$$
N_{*}=\begin{cases} [ \frac{2n}{n+2}, + \infty) \text{ für }n\geq 3,\\
(1,+\infty) \text{ für } n=2, \\
[1,+\infty] \text{ für }n=1
\end{cases}
$$
gegeben.
Dann ist die Einbettung $H^1(\Omega)\hookrightarrow L^p(\Omega)$ stetig für alle $p \in N^*$. 
Wir sagen, dass $(p,q)$ ein *zulässiges Paar* ist, wenn $p \in N^*$ und $\frac{1}{p}+\frac{1}{q}=1$ gilt.
Nach Konstruktion ist dann automatisch $q \in N_{*}$.
Der Vorteil dieser Notation ist, dass für zulässige Paare das Produkt der Funktionen $f \in L^p(\Omega)$ und $g \in L^q(\Omega)$ $fg\in L^1(\Omega)$ nach der Hölder-Ungleichung.