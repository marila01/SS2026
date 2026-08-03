# a)

Betrachte für $v,u \in V$
$$
|\langle A(u),v\rangle| \leq \int_{\Omega}|a(x,\nabla u)||\nabla v|\,dx \leq C\int_{\Omega}(1+|\nabla u|^{p-1})|\nabla v|\,dx = C \int_{\Omega}|\nabla v|\,dx+C\int_{\Omega}|\nabla u|^{p-1}|\nabla v|\,dx
$$
Da $|\Omega|<\infty$ und $p>1$ gilt $L^p(\Omega)\hookrightarrow L^1(\Omega)$, daher ist das erste Integral endlich und wegen der Einbettung existiert $D>0$ sodass $||\nabla v||_{L^{1}(\Omega)}\leq D||\nabla v||_{L^p(\Omega)}$.

Sei $q$ derart, dass $1/q + 1/p=1$. Dann ist $q = p/(p-1)$ und $|\nabla u|^{p-1} \in L^q(\Omega)$ bzw. $||\nabla u||^{p-1}_{L^p(\Omega)}=||\,|\nabla u|^{p-1}\,||_{L^q(\Omega)}$
Wegen Hölder folgt dann 
$$
\int_{\Omega}|\nabla u|^{p-1}|\nabla v|\,dx \leq ||\,|\nabla u|^{p-1}||_{L^q(\Omega)}||\nabla v||_{L^p(\Omega)}\leq ||\nabla u||^{p-1}_{L^p(\Omega)}||\nabla v||_{L^p(\Omega)}
$$
Insgesamt erhält man mit Poincare
$$
|\langle A(u),v\rangle| \leq C(D||\nabla v||_{L^p(\Omega)}+||\,|\nabla u|^{p-1}\,||_{L^q(\Omega)}||\nabla v||_{L^p(\Omega)})\leq C E(D+E^{p-1}|| u||^{p-1}_{W^{1,p}(\Omega)})||v||_{W^{1,p}(\Omega)} < \infty
$$

# b)
$A$ is hemi-continous.
Für $u,v,w\in V$ und $t \in [0,1]$ und $t_k\to t$ gilt punktweise fast überall
$$
a(x,\nabla u+t_{k}\nabla v)\to a(x,\nabla u+t\nabla v)
$$
da $a$ Caratheordory.
Der Integrand ist analog zur Argumentation in a) in $L^1$ unabhängig von $k$, da $|t_k|<1$.
Aus dominierter Konvergenz folgt dann die Behauptung.

# c)
$A$ ist monoton, da
$$
\langle A(u)-A(v),u-v \rangle = \int_{\Omega}\underbrace{(a(x,\nabla u)-a(x,\nabla v))(\nabla u-\nabla v)}_{\geq 0}\,dx\geq 0
$$
# d)
$A$ ist coercive, da für $||u||_V\to \infty$ gilt mit Poincare
$$
\frac{\langle A(u),u\rangle}{||u||_{V}}\geq \frac{1}{||u||_{V}}\int_{\Omega} c|\nabla u | ^p-C\,dx = c\frac{||\nabla u||^p_{L^p(\Omega)}}{||u||_{V}}-|\Omega|C \frac{1}{||u||_{V}} \geq Dc ||u||^{p-1}_{W^{1,p}(\Omega)}-|\Omega|C \frac{1}{||u||_{V}}\to \infty
$$

# e)
Angenommen es gibt $u,v \in V, u \neq v$ sodass
$$
\langle A(u)-A(v),u-v\rangle = \int_{\Omega}\underbrace{(a(x,\nabla u)-a(x,\nabla v))(\nabla u-\nabla v)}_{\geq 0}\,dx= 0
$$
Dann gilt fast überall
$$
(a(x,\nabla u)-a(x,\nabla v))(\nabla u-\nabla v) = 0
$$
(Auf der Nullmenge definieren wir einfach um)
also nach Voraussetzung 
$$
\nabla u = \nabla v
$$
und da $V = W_0^{1,p}(\Omega)$ schon  $u=v$. Widerspruch.

# g)
Nach Lemma 3.21 ist $A$ Type M, da hemistetig und monoton.

# f)
Sei $u_{k}\rightharpoonup u$ in $V$.
Da $A$ nach a) beschränkt ist, gibt es nach Eberlein-Smulian eine Teilfolge $u_{k'}$ mit $A(u_{k'})\rightharpoonup b$ w-$V^*$.
Dann gilt
$$
\limsup \langle A(u_{k'}),u_{k'}\rangle =\underbrace{\limsup \langle A(u_{k'}),u_{k'}-u\rangle+}_{\leq 0}\limsup\langle A(u_{k'}),u\rangle \leq \langle b,u\rangle
$$
Da $A$ Type-M ist, gilt $A(u)=b$ 
Da man das für jede Teilfolge einer Teilfolge machen kann, gilt wegen Uryson
$$
A(u_{k})\rightharpoonup A(u).
$$ 
# h)
Wegen Lemma 3.23 vererben sich die Eigenschaften monton, koerziv, beschränkt und Typ-M auf den Ort-Zeit Operator.
Wegen Theorem 3.22 gibt es eine Lösung für $u_0 \in L^2(\Omega)$, wobei $W^{1,p}(\Omega)\hookrightarrow L^2(\Omega)$ für $p> \frac{2n}{n+2}$ und $f \in L^q(0,T; V')$.
Wegen Theorem 3.24 ist diese Lösung eindeutig.