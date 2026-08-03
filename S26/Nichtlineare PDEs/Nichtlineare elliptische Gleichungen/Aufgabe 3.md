# a)
$$
|\langle B(u),v\rangle| \leq \int_{\Omega}|u|^{q-1}|v|\,dx
$$
Es gilt $|u|^{q-1}\in L^{q'}(\Omega)$, da $||\,|u|^{q-1}\,||_{L^{q'}(\Omega)}=\left(||u||_{L^{q}(\Omega)}\right)^{q-1}$.
Da $W^{1,p}(\Omega)\hookrightarrow L^q(\Omega)$ für $q<p^*$ ist $v\in L^q(\Omega)$ und $||v||_{L^q(\Omega)}\leq C||v||_{W^{1,p}(\Omega)}$ für ein $C>0$.

Folglich kann man Hölder anwenden und es gilt
$$
\begin{align}
\int_{\Omega}|u|^{q-1}|v|\,dx&\leq ||\,|u|^{q-1}||_{L^{q'}(\Omega)}||v||_{L^q(\Omega)}\\&\leq C\left(||u||_{L^{q}(\Omega)}\right)^{q-1}||v||_{W^{1,p}(\Omega)}\\&<C^q (||u||_{W^{1,p}(\Omega)})^{q-1}||v||_{W^{1,p}(\Omega)}<\infty.
\end{align}
$$
Deshalb ist $B$ beschränkt in $u$. Außerdem ist $B$ klarerweise linear und beschränkt in $v$ und daher stetig.
Deshalb ist $B:V\to V'$ wohldefiniert und man kann auch alle Sätze, die wir allgemein gezeigt haben, anwenden.

# b) 
$B$ ist monoton, da man durch differenzieren erhält, dass $|x|^{q-2}x$ monoton ist.
Durch Fallunterscheidung nach Vorzeichen erhält man punktweise
$$
(|u|^{q-2} u-|v|^{q-2} v)(u-v)\geq 0 \quad \forall u,v \in V
$$
und Integrieren erhält die Ungleichung.

# c)
Für $u,v,w\in V$ und $t\in [0,1]$ und $t_k \to t$ gilt, dass $|u+t_k v|^{q-2}|(u+t_k v)\to |u+tv|^{q-2}(u+tv)$, da stetig. (?)
Aus majorisierter Konvergenz folgt die Behauptung, wegen in wie in a) und 2b.

# d)
Das Folgt im Wesentlichen alles aus a), b), c) und  Beispiel 3.18, wo alle Eigenschaften für $A$ nachgerechnet werden.

# e) 
$T$ ist koerziv, da 
$$
\frac{\langle T(u),u \rangle}{||u||_{V}}=  \underbrace{\frac{||u||_{L^q(\Omega)}^q}{||u||_{V}}}_{\geq 0}+ \langle A(u),u\rangle \to \infty
$$
für $||u||_{V}\to \infty$, weil $A$ koerziv ist.

# f)
Das folgt aus Lemma 3.21, da $T$ hemistetig und monoton ist.

# g) 
Wegen Lemma 3.23 vererben sich hemistetig, monoton, beschänkt, Type-M und koerziv auf den Zeit-Ort-Operator.
Wegen Theorem 3.22 gibt es eine Lösung.

Variationelle Formulieung
$$
\int_{0}^T \langle u_{t},v\rangle dt + \int_{0}^T\langle T(u),v\rangle dt = \int_{0}^T \langle f,v\rangle dt
$$
Und
$$
\int_{0}^t \langle T(u),u\rangle dt \geq \int_{0}^t \underbrace{\langle B(u),u\rangle\,ds}_{\geq 0}+C\int_{0}^t||u||_{V}^p\,ds
$$