Sei $u \in D^1(I,\mathbb{R}^N)$ und $\forall v \in C_{r}:\mathcal{F}(u)\leq \mathcal{F}(v)$ für ein $r>0$ und
$$
C_{r=}\{v \in D^1(I,\mathbb{R}^N)|v(a)=u(a),v(b)=u(b), \mathrm{sup}_{I}|u-v|<r  \}.
$$
Sei $x \in (a,b)$ eine Ecke von $u$, $z_{0}:=u(x_{0})$, $p_{0}^{\pm}:=u'(x_{0}\pm_{0})$
Dann gelten die zwei Erdmann'schen Eckbedinungen:
- $\nabla_{p}F(x_{0},z_{0},p_{0}^+)=\nabla_{p}F(x_{0},z_{0},p_{0}^-)$ (Stetigkeit vom $p$-Gradienten obwohl die Ableitung unstetig ist).
- $F(x_{0},z_{0},p_{0}^-)-p_{0}^-\nabla_{p}F(x_{0},z_{0},p_{0}^-)=F(x_{0},z_{0},p_{0}^+)-p_{0}^+\nabla_{p}F(x_{0},z_{0},p_{0}^+)$
##### Beweis:
**(a)**
$$
\begin{align}
0 &=\delta \mathcal{F}(u,\xi)\quad\forall \xi \in C_{0}^\infty \\
&=\int_{a}^b [\nabla_{z}F(x,u(x),u'(x))\cdot \xi+\nabla_{p}F(x,u(x),u'(x))\cdot \xi'(x)]dx
\end{align}
$$
Da der Integrand zwar nicht stetig aber zumindest $L^\infty$ ist, kann man die Ableitung nach $z$ nicht nochmal differenzieren, wie in [[Satz 2.30]].
Daher integriert man dieses Ausdruck und leitet $\xi$ ab.
Das liefert:
$$
\int_{a}^b \left[ -\int_{a}^x \nabla_{z}F(t,u(t),u'(t))dt+\nabla_{p}F(x,u(x),u'(x)) \right]\cdot \xi'(x)dx
$$
Aus dem [[Lemma 2.24 (Fundamentallemma)]] (c) folgt dann
$$
-\int_{a}^x\nabla_{z}F(t,u(t),u'(t))dt+\nabla_{p}F(x,u(x),u'(x))=const.\in \mathbb{R}^N\text{ f.ü.}
$$
$\implies \nabla_{p}F(x,u(x),u'(x))=C+\int_{a}^b\nabla_{z}F(t,u(t),u'(t))dt \text{ f.ü.}$
Das Integral einer $L^\infty$ - Funktion ist stetig, also ist auch $\nabla_{p}F(x,u(x),u'(x))$ stetig.

*Bemerkung: Hier ist der Knick additiv, da die Störung glatt ist, befindet er sich an derselben Stelle. Bei (b) betrachten wir innere Variablen und somit eine völlig andere Art von Störungen.*

**(b)**
