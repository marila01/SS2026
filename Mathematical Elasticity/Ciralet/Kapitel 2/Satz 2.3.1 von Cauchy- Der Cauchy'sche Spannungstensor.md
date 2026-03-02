Sei $f^\Phi:\bar{\Omega}^\Phi \to \mathbb{R}^3$ stetig und das Cauchy'sche Spannungsvektorfeld $t^\Phi:\bar{\Omega}^\Phi \to \mathbb{R}^3$ stetig differenzierbar im ersten Argument sowie stetig im zweiten Argument.
Dann implizieren die Axioms of force and moment balance die Existenz eines stetig differenzierbaren Tensorfelds $T^\Phi:\bar{\Omega}^\Phi \to \mathbb{M}^3, x^\Phi \mapsto T^\Phi(x^\Phi)$, sodass gilt
1.  $\forall x^\Phi \in \bar{\Omega}^\Phi,n \in S_{1}: t^\Phi(x^\Phi,n)=T^\Phi(x^\Phi)n$
2.  $\forall x^\Phi \in \Omega^\Phi:-\mathrm{div}^\Phi(T^\Phi(x^\Phi))=f^\Phi(x^\Phi)$
3. $\forall x^\Phi \in \bar{\Omega}^\Phi:T^\Phi(x^\Phi)=(T^\Phi(x^\Phi))^T.$
4.  $\forall x^\Phi \in \Gamma_{1}^\Phi:T^\Phi(x^\Phi)n^\Phi=g^\Phi(x^\Phi)$, $n^\Phi$ äußerer Normalenvektor auf $\Gamma_{1}^\Phi$.
#### Beweis:
![[Pasted image 20260215122215.png]]
##### 1)
Sei $x^\Phi \in \Omega^\Phi$ fest. Da $\Omega ^\Phi$ offen, findet man ein Tetraeder $T$ mit Eckpunkt $x^\Phi$ und Seitenflächen parallel zu den Koordinatenebenen sowie einer vorderen Fläche, deren Normalvektor $n=\sum_{i}n_{i}e_{i}$ Komponenten $n_{i}>0$ hat.
Seien $v_{i}$ die restlichen Eckpunkte, $F_{i}$ die Flächen gegenüber von $v_{i}$, sodass $\mathrm{area}(F_{i})=n_{i}\mathrm{area}(F)$.

Das Axiom of force balance über $T$ liefert $$\int_{T}f^\Phi(y^\Phi)\mathrm{d}y^\Phi+\int_{\partial T}t^\Phi(y^\Phi,n^\Phi)\mathrm{d}a^\Phi=0.$$
Schreibt man das komponentenweise mittels $f^\Phi(y^\phi)=\sum_{i}f_{i}^\Phi(y^\Phi)e_{i}$, $t^\Phi(y^\Phi,n^\Phi)=\sum_{i}t_{i}^\Phi(y^\Phi,n^\Phi)e_{i}$ und verwendet man den Mittelwertsatz für Integrale (auf das Integral über $\partial T$, die betreffenden Funktionen sind ja stetig), erhält man nach einigen Zwischenschritten ([[SatzVCauchyRechnung.pdf]]) für $i=1,2,3$ sowie für geeignete $y_{i}\in F,y_{ij}\in F_{j},j=1,2,3$
$$|t^\Phi_{i}(y_{i},n)+\sum_{j} t^\Phi_{i}(y_{ij},-e_{j})n_{j}|\mathrm{area}(F)\leq \mathrm{sup}_{y\in T}|f_{i}^\Phi(y)|\mathrm{vol}(T).$$
Hält man nun $n$ fest und lässt die $v_{i}$ jeweils gegen $x^\Phi$ gehen, erhält man daraus, weil $t^\Phi$ stetig in $x^\Phi$ und $\mathrm{vol}(T)\leq c(n)(\mathrm{area}(F))^\frac{3}{2}$ sowie $f^\Phi$ beschränkt ist,
$$t^\Phi(x^\Phi,n)=-\sum_{j}n_{j}t^\Phi(x^\Phi,-e_{j}).$$
Da $t^\Phi$ auch stetig in $n$ ist, erhält man für $n \to e_{j},j=1,2,3$
$$t^\Phi(x^\Phi,e_{j})=-t^\Phi(x^\Phi,-e_{j}).$$
D.h. für $n_{i}<0$ gilt
$$t^\Phi(x^\Phi,n)=\sum_{j}n_{j}t^\Phi(x^\Phi,e_{j}).$$
Also gilt die Gleichheit für alle $x^\Phi \in \bar{\Omega}^\Phi$ und $n\in S_{1}$.
Wir definieren nun $T^\Phi_{ij}:\bar{\Omega}^\Phi\to \mathbb{R}$ mittels $t^\Phi(x^\Phi,e_{j})=\sum_{j}T^\Phi_{ij}(x^\Phi)n_{j}$ also $t^\Phi(x^\Phi,n)=\sum_{i,j}T^\Phi_{ij}(x^\Phi)n_{j}e_{i}$.
Daher $t_{i}^\Phi(x^\Phi,n)=\sum_{j}T^\Phi_{ij}(x^\Phi)n_{j}$ für alle $x^\Phi \in \bar{\Omega}^\Phi$ und $n \in S_{1}$.
Setze nun $T^\Phi(x^\Phi):=(T^\Phi_{ij}(x^\Phi))_{i,j}$.
Dann sind die Gleichungen $\forall i=1,2,3: t^\Phi_{i}(x^\Phi,n)=\sum_{j}T^\Phi_{ij}(x^\Phi)n_{j}$ äquivalent zu
$$t^\Phi(x^\Phi,n)=T^\Phi(x^\Phi)n.$$
Das gilt erstmal nur für $x^\Phi \in \Omega ^\Phi$ (offen) und $n \in S_{1}$, wobei $|n_{i}|\neq 0$.
Aus Stetigkeitsgründen gilt das aber sogar auf ganz $\bar{\Omega}^\Phi$ bzw. $S_{1}$.
Da $t^\Phi(x^\Phi,e_{j})=\sum_{i}T_{ij}^\Phi(x^\Phi)e_{i}$, ist $T^\Phi$ genauso glatt in $x^\Phi$ wie $t^\Phi$.
##### 2)
Der Divergenzsatz für Tensorfelder aus Sect.1.7. in Ciralet angewandt auf $T^\Phi$ rechtfertigt die Transformation von Oberflächenintegralen in Volumsintegrale:
$$\forall A^\Phi \subset \Omega ^\Phi: \int_{\partial A^\Phi}t^\Phi(x^\Phi,n^\Phi)\mathrm{d}a^\Phi=\int_{\partial A^\Phi}T^\Phi(x^\Phi)n^\Phi \mathrm{d}a^\Phi=\int_{A^\Phi}\mathrm{div}^\Phi (T^\Phi(x^\Phi))\mathrm{d}x^\Phi.$$
Das Axiom of force balance sagt dann $\forall A^\Phi \subset \Omega ^\Phi:\int_{A^\Phi}[\mathrm{div}^\Phi(T^\Phi(x^\Phi))+f^\Phi(x^\Phi)]\mathrm{d}x^\Phi=0$.

also folgt
$$\forall x^\Phi \in \Omega ^\Phi:\mathrm{div}^\Phi(T^\Phi(x^\Phi))+f^\Phi(x^\Phi)=0$$

##### 3)
Mit der Greene'schen Integralformel kann man auch die Oberflächenintegrale vom Axiom of moment balance transformieren, denn für $i \neq j$ gilt, komponentenweise betrachtet und nach Auflösen des Kreuzprodukts sowie anwenden der Produktregel:
$$
\begin{align*}
\int_{\partial A^\Phi}[x_{j}^\Phi t_{i}^\Phi(x^\Phi,n^\Phi)-x_{i}^\Phi t_{j}^\Phi(x^\Phi,n^\Phi)]\mathrm{d}a^\Phi &= \int_{\partial A^\Phi}\sum_{k}[x_{j}^\Phi T_{ik}^\Phi(x^\Phi)-x_{i}^\Phi T_{jk}^\Phi(x^\Phi)]n_{k}\mathrm{d}a^\Phi \\
&=\int_{A^\Phi}\sum_{k}\partial_{k}[x_{j}^\Phi T_{ik}^\Phi(x^\Phi)-x_{i}^\Phi T_{jk}^\Phi(x^\Phi)]\mathrm{d}x^\Phi \\
&=\int_{A^\Phi}\left[ \sum_{k}(\delta_{jk}T_{ik}^\Phi(x^\Phi)-\delta_{ik}T^\Phi_{jk}(x^\Phi))+(x_{j}\partial_{k}T_{ik}^\Phi(x^\Phi)-x_{i}^\Phi\partial_{k}T_{jk}^\Phi(x^\Phi)) \right]\mathrm{d}x^\Phi\\
&=\int_{A^\Phi}[T_{ij}^\Phi(x^\Phi)-T_{ji}^\Phi(x^\Phi)]-[x_{j}^\Phi f_{i}^\Phi(x^\Phi)-x_{i}^\Phi f_{j}^\Phi(x^\Phi)]]\mathrm{d}x^\Phi

\end{align*}
$$
Wegen 2) folgt
$$
\forall A^\Phi \subset \Omega^\Phi:\int_{A^\Phi}[T_{ij}^\Phi(x^\Phi)-T_{ji}^\Phi(x^\Phi)]\mathrm{d}x^\Phi=0 \implies T^\Phi=(T^\Phi)^T.
$$
##### 4)
Die Randbedingung $\forall x^\Phi \in \Gamma_{1}^\Phi:T^\Phi(x^\Phi)n^\Phi=g^\Phi(x^\Phi)$ kommt direkt aus dem ersten Punkt der Definition des Cauchy Stress Vektors [[Fundamental Stress Principle of Euler and Cauchy#^3f1f65]].

#### Bemerkungen
- Die Existenz und die Vektorgleichung folgen also aus der Stetigkeit von $t^\Phi$ in den *einzelnen* Variablen und dem Axiom of force Balance.
- Die Divergenzgleichung folgt aus dem Axiom of force balance.
- Die stetige Differnzierbarkeit von $t^\Phi$ braucht man vor allem für di Symmetrie von $T^\Phi$.
- $T^\Phi$ nennt man den Cauchy-Stress-Tensor/ Cauchy'schen Spannungstensor.
- Eine visuelle Interpretation zum Cauchy'schen Spannungstensor findet man hier: https://youtu.be/NtTVEzZS3Bg?si=FM0NfbnNPrEq5pAV.