Seien $B$ ein Banachraum, $K \subset B$ eine kompakte und konvexe Menge und $S:K\to K$ eine stetige Abbildung. Dann besitzt $S$ einen Fixpunkt.

##### Bemerkungen:
- $K$ kompakt $\iff$ Jede offene Überdeckung hat eine endliche Teilüberdeckung.
- Da $B$ Banach: $\iff$ Jede Folge in $K$ hat eine konvergente Teilfolge.
- $K$ konvex $\iff \forall \lambda \in[0,1], u,v \in K:\lambda u+(1-\lambda)v\in K$
- Man bekommt keinen eindeutigen Fixpunkt.
#### Beweis
Wir geben nur die Beweisidee. Ein vollständiger Beweis findet sich in Gilbarg-Trüdinger 11, Sec. 11.1. Der Beweis basiert auf [[Theorem 2.4 (Fixpunkt von Brower)]].
Betrachte für festes $j \in \mathbb{N}$ die Kugeln $\left( B_{\frac{1}{j}} (x)\right)$ für jedes $x \in K$.
Das ist eine offene Überdeckung von $K$.
Da $K$ kompakt, existieren für gegebenes $j\in \mathbb{N}$ Punkte $x_{1},\dots,x_{N_{j}}$, sodass die Kugeln $B_{\frac{1}{j}}(x_{i}),i=1,\dots,N_{j}$, die Menge $K$ überdecken, also $K \subset \bigcup_{k=1}^{N_{j}}B_{\frac{1}{j}}(x_{k})$.

Sei $K_{j} \subset K$ die konvexe Hülle von $\{ x_{1},\dots,x_{N_{j}} \}$ und $(\lambda_{r})_{r=1,\dots,N_{j}}$ eine smooth partition of unity zu dieser Überdeckung.
Definiere $F_{j}:B\to K_{j};F_{j}(x):=\sum_{r=1}^{N_{j}}\lambda_{r}(x)x_{r}$. 
Das ganze mit der konvexen Hülle machen wir, damit unser Problem gewissermaßen endlichdimensional ist, sodass wir Brouwer anwenden können.

*Behauptung: (wir beweisen das nicht extra)* Man kann $F_{j}$ so konstruieren, dass $||F_{j}(x)-x||\leq \frac{1}{j}$, daher ist $F_{j}$ eine quasi Approximation der Identität mit Wertebereich in $K_{j}$.

Da $K$ konvex, gilt $K_{j}\subset K$.
Dann ist $F_{j}\circ S_{|_{K_{j}}}$ nach Konstruktion eine stetige Abbildung von $K_{j}\to K_{j}$. 
Nach dem Satz von Brower besitzt diese Abbildung einen Fixpunkt $u_{j}\in K_{j}\subset K$.
Da das für jedes $j$ gilt, erhalten wir eine Folge $(u_{j})$ von Fixpunkten.
Da $K$ kompakt ist, konvergiert eine Teilfolge $(u_{j'})$ gegen ein $u^*\in K$ und da die $u_{j'}$ jeweils Fixpunkte sind, folgt aus dem (nicht bewiesenen) claim:

$$ \begin{align}
||u_{j'}-S(u_{j'})|| &= ||F_{j'}\circ S_{|K_{j}}(u_{j'})-S(u_{j'})|| \\
&=||F_{j'}\circ S (u_{j'})-S(u_{j'})|| \\
&\leq \frac{1}{j'}\to 0 \text{ für } j'\to +\infty.
\end{align}
$$
Mittels Dreiecksungleichung folgt nun:
$$
||u^*-S(u^*)||\leq ||u^*-u_{j'}||+||u_{j'}-S(u_{j'})||+||S(u_{j'})-S(u^*)||
$$
Der erste Term geht gegen null wegen $u_{j'}\to u^*$, der zweite wegen obiger Ungleichungskette und dritte wegen $u_{j'}\to u^*$ und $S$ stetig.