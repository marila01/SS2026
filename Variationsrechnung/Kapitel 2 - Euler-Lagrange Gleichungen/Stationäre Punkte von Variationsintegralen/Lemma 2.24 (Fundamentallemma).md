Sei $\Omega \subset \mathbb{R}^n$ offen, $f \in C(\Omega,\mathbb{R})$ und
1. $\int_{\Omega}f\eta dx\geq 0 \forall \eta \in C_{0}^\infty(\Omega), \eta \geq 0 \implies f\geq 0.$
2. $\int_{\Omega}f\eta dx=0$ $\forall \eta \in C_{0}^\infty(\Omega) \implies f=0$.
3. *(Du Boid-Reymond Lemma)* Sei $\Omega$ auch zusammenhängend, $f \in C^1(\Omega,\mathbb{R})$ und $\int_{\Omega}f(x)\frac{\partial \eta}{\partial x_{j}}(x)dx=0, \quad 1\leq j\leq n,\forall \eta \in C_{0}^\infty(\Omega)\implies f=const.$ auf $\Omega$.
##### Beweis:
Es gelte die erste Voraussetzung. Angenommen es existiere $x_{0}\in \Omega$ mit $f(x_{0})<0$.
$\implies \exists \varepsilon,r>0$ mit $\bar{B_{r}(x_{0})}\subset \Omega$ und $f(x)<-\varepsilon$ $\forall x \in B_{r}(x_{0})$.
Wähle
$$
\eta(x):=\begin{cases}
\mathrm{exp}\left( -\frac{1}{r^2-|x-x_{0}|^2} \right) \quad x \in B_{r}(x_{0}), \\
0 \quad \text{sonst.} \\
\end{cases}
$$
Dann ist $\eta \in C_{0}^\infty(\Omega), \eta\geq 0$.
$$
\int_{\Omega}f\eta dx=\int_{B_{r}(x_{0})}f\eta dx<-\varepsilon \int_{B_{r}(x_{0})}\eta dx<0
$$
Widerspruch zur Annahme, also $f=0$.

Wenn die zweite Voraussetzung gilt, gilt die erste für $f$ und $-f$, also $f=0$.

Die letzte Voraussetzung folgt aus der zweiten mit partieller Integration.