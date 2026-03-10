Sei $\partial \Omega \in C^1, F \in C^1(V; \mathbb{R}^N), \frac{\partial F}{\partial p_{ij}}\in C^1(V), u \in C^2(\Omega;\mathbb{R}^N)\cap C^1(\bar{\Omega};\mathbb{R}^n).$
Falls $\forall \xi \in C^\infty(\bar{\Omega})$: $\delta F(u,\xi)=0$ gilt, erfüllt $u$ auf $\Omega$ die EL-Gl. von $\mathcal{F}$ und auf $\partial \Omega$ die *natürlichen Randbedingungen*:
$$
\sum_{j=1}^n\nu_{j}(x)\frac{\partial F}{\partial p_{ij}}(x,u(x),Du(x))=0\quad i=1,\dots,N 
$$
wobei $\nu(x)$ der äußere Normalenvektor im Punkt $x$ auf $\partial \Omega$ ist.

##### Beweis:
**Schritt 1**:
Sei $u \in C^2(\bar{\Omega};\mathbb{R}^N)$. Das ist eine wesentliche Einschränkung (vgl. Regularitätsresultate bei PDEs), die in Schritt 2 behandelt wird.
Sei $\xi(x)=\psi(x)e_{i},\psi \in C^\infty(\bar{\Omega})$. Mit partieller Integration folgt:
$$
\begin{align} \\
0 &= \delta \mathcal{F}(u,\xi) \\
&= \int_{\Omega} \frac{\partial F}{\partial z_{i}}\psi+\sum_{j=1}^n\frac{\partial F}{\partial p_{ij}}\frac{\partial \psi}{\partial x_{j}}  dx \\
\int_{\Omega}L_{F}(u)_{i}\psi dx+\int_{\partial \Omega}\sum_{j=1}^n\nu_{j}(x)\frac{\partial F}{\partial p_{ij}}(x,u(x),Du(x))dS 
\end{align} \\
$$
Das gilt für alle $\xi \in C^\infty(\bar{\Omega})$, insbesondere für $\xi \in C_{0}^\infty(\Omega)$, also können wir aus [[Satz 2.23]] folgern, dass das erste Integral verschwindet.
Da der Integrand des Oberflächenintegrals stetig ist, kann man aus dem Analogon der Variationslemmas für Oberflächenintegrale folgern
$$
\sum_{j=1}^n \nu_{j}(x)\frac{\partial F}{\partial p_{ij}}(x,u(x), Du(x))=0 
$$

**Schritt 2:**
Für $u \not\in C^2(\bar{\Omega})$ kann man nicht partiell integrieren, da $\mathrm{div}\left( \psi \frac{\partial F}{\partial p_{ij}} \right) \not\in C(\bar{\Omega})$.
Man approximiert daher $\Omega$ von innen mit Mengen $\Omega_{k}\subset  \bar{\Omega_{k}} \subset \Omega, \Omega_{k}\uparrow \Omega, \partial \Omega_{k}\in C^1$ und $\partial \Omega_{k}\to \partial \Omega$ für $k \to \infty$ in $C^1$.
Man kann ja die Ränder lokal als Graphen von $C^1$-Funktionen darstellen. Konvergenz der Ränder bedeutet, dass diese Funktionen konvergieren.

Auf diesen Mengen kann gilt bereits das in Schritt 1 bewiesene.
Das rigoros zu zeigen, ist aufwändig und wird daher nicht in der Vorlesung gemacht.