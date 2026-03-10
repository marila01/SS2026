---
aliases:
  - "Definition 1.1.: Sobolevräume"
---
Seien $m \in \mathbb{N}_{0}$ und $1\leq p\leq \infty$. Der Sobolevraum $W^{m,p}(\Omega)$ ist die Menge aller Funktionen $u \in L^p(\Omega)$, sodass 
$$
D^\alpha u\in L^p(\Omega) \text{ für alle } |\alpha|\leq m,
$$
wobei $\alpha$ ein Multiindex und $D^\alpha u$ die entsprechende partielle Ableitung von $u$ im Sinne der Distributionen sind.

Eigentlich sind das Äquivalenzklassen von Funktionen, die auf Nullmengen übereinstimmen.

Auf $W^{m,p}(\Omega)$ ist die Norm
$$
||u||_{W^{m,p}(\Omega)}^p:=\sum_{|\alpha|\leq m}||D^\alpha u||^p_{L^p(\Omega)}, \text{ falls } p<\infty,
$$
$$
||u||_{W^{m,p}(\Omega)}:=\mathrm{max}_{|\alpha|\leq m}||D^\alpha u||_{L^p(\Omega)}, \text{ p=} \infty,
$$
defniert.

Mit dieser Norm ist $W^{m,p}(\Omega)$ ein Banachraum.
Im Falle $m=0$ betrachten wir genau die $L^p(\Omega)$-Räume.
Für $p=2$ setzen wir $H^m(\Omega)=W^{m,2}(\Omega)$.
Dieser Raum ist mit der Summe der $L^2$-Skalarprodukte der Ableitungen ein Hilbertraum.