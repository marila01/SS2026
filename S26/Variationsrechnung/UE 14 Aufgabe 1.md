Sei $1 \leq p \leq \infty$ und $u_{j}\rightharpoonup u$ w-$L^p(\Omega,\mathbb{R}^m)$ (bzw. $\stackrel{*}{\rightharpoonup}$ in $L^\infty(\Omega, \mathbb{R}^m)$).
z.z.  Es gibt eine Teilfolge von $u_{j}$ und ein Young-Maß $\nu$, und es gilt
$$
u(x)= \int_{\mathbb{R}^m}\lambda d\nu_{x}(\lambda)
$$
für fast alle $x \in \Omega$.

### 1.
Wir zeigen zuerst, dass es eine straffe Teilfolge $u_{jk}$ gibt, damit wir den Satz anwenden können.

Für $p = \infty$ ist die Aussage trivial.


![[Pasted image 20260624183457.png]]
Für $p = 1$ kann man Dunford-Pettis anwenden, dann ist diese Folge UI, was für $p=1$ dasselbe ist wie dass die Teilfolge straff ist.

Für $p> 1$ gilt $L^p(\Omega)\subset L^1(\Omega)$ und die Folge ist beschränkt in $L^p$ und daher auch UI in $L^1(\Omega)$.

Wegen dem Satz gibt es in jedem Fall eine Teilfolge $u_{j_{k}}$, die ein Young-Maß erzeugt und für alle 
$$
g \in L^1(\Omega), f \in C_{0}(\mathbb{R}^m): \int_{\Omega}g f(u_{j_{k}})dx\to \int_{\Omega}g(x)\left( \int_{\mathbb{R}^m} fd\nu(x)\right)dx
$$
(Das hängt nicht von $p$ ab, deshalb reicht es für $p>1$ nur $L^1$ anzusehen)

### 2. 
Sei nun $g \in L^q(\Omega) \subset L^1(\Omega)$ beliebig. Testen wir gegen beliebiges $g$ und beim Testen Gleichheit, erhalten wir Gleichheit fast überall. 
Für beliebiges $R> 0$ definiere $f_{R}(\lambda)=\phi_{R}(\lambda)\lambda$, wobei $\phi_{R}$ eine Cutoff-Funktion mit $0 \leq \phi_{R}\leq 1$, $\phi_{R}(\lambda)=1$ für $|\lambda|\leq R$, $\text{supp}\,\phi_{R}\subset B_{2R}(0)$ mit $\phi_{R}\in C_{0}^\infty(\mathbb{R}^m)$.
Dann ist $f_{R}\in C_{0}(\mathbb{R}^m)$.

Komponentenweise kann man den Young-Maße Satz anwenden und es gilt insgesamt:
$$
\langle g, \phi_{R}(u_{j_{k_{\ell}}})u_{j_{k_{\ell}}}\rangle =
\int_{\Omega}g(x)\phi_{R}(u_{j_{k}}(x))u_{j_{k}}(x)dx \to \int_{\Omega}g(x)(\int_{\mathbb{R}^m}\phi_{R}(\lambda)\lambda d\nu(x))dx = \langle g, \int_{\mathbb{R}^m}\phi_{R}(\lambda)\lambda d\nu_{(.)}(\lambda)dx\rangle
$$
Da $u_{j_{k_{\ell}}}\rightharpoonup u$, gilt auch 
$$
\langle g, u_{j_{k_{\ell}}}\rangle \to \langle g,u\rangle
$$
Es gilt
$$
u_{j_{k}}-\phi_{R}(u_{j_{k}})u_{j_{k}}= (1-\phi_{R}(u_{j_{k}}))u_{j_{k}}
$$
wobei dieser Ausdruck auf $\{ |u_{j_{k}}|\leq R \}$ verschwindet.
Außerdem gilt 
$$
|u_{j_{k}}-\phi_{R}(u_{j_{k}})u_{j_{k}}|\leq 2 \cdot \mathbb{1}_{\{ |u_{j_{k}}|>R \}}|u_{j_{k}}|.
$$
Daher 
$$
|\int_{\Omega}g\cdot(u_{j_{k}}-\phi_{R}(u_{j_{k}})u_{j_{k}})\,dx| \leq 2 \int_{\{ |u_{j_{k}}|>R \}} |g||u_{j_{k}}|\,dx
$$
Dieser Ausdruck verschwindet für $R\to \infty$:

Falls $p =1$ ist die Hölder-Konjugierte $q=\infty$.
Daher
$$
\int_{\{ |u_{j_{k}}|>R \}}|g||u_{j_{k}}|\,dx \leq ||g||_{L^\infty}\int_{\{ |u_{j_{k}}|>R \}}|u_{j_{k}}|\,dx
$$
Da $u_{j_{k}}$ gleichgradig integrierbar ist, gilt für $R\to \infty$
$$
\sup_{k}\int_{\{ |u_{j_{k}}|>R \}}|u_{j_{k}}|\,dx\to 0,
$$
weswegen der ganze (gewünschte) Term oben glm. in $k$ gegen $0$ geht.

Falls $1<p<\infty$, ist $(u_{j_{k}})$ $L^p-$beschränkt, also $\sup_{j}||u_{j_{k}}||_{L^p}\leq C$.
Sei $M> 0$. Dann
$$
\int_{\{ |u_{j_{k}}|>R \}} |g||u_{j_{k}}|\,dx \leq M \int_{\{ |u_{j_{k}}|>R \}}|u_{j_{k}}|\,dx + \int_{\{ |g| >M \}}|g||u_{j_{k}}|\,dx
$$
Den ersten Term kann man folgendermaßen abschätzen:
$$
M\int_{\{ |u_{j_{k}}|>R \}}|u_{j_{k}}|\,dx\leq M\frac{1}{R^{p-1}}\int_{\Omega}|u_{j_{k}}|^p\,dx \leq \frac{C}{R^{p-1}}M\to 0
$$
Für den zweiten Term kann man Hölder verwenden
$$
\int_{\{ |g|>M \}}|g||u_{j_{k}}|\,dx\leq||g \cdot\mathbb{1}_{\{ |g|>M \}}||_{L^q}||u_{j_{k}}||_{L^p}\leq C ||g\cdot\mathbb{1}_{\{ |g|>M \}}||_{L^q}
$$
d.h. dieser Term geht für $M\to \infty$ wegen dominierter Konvergenz gegen 0.
Insgesamt geht also auch dieser Term glm. in $k$ für $R\to \infty$ gegen $0$.

Falls $p= \infty$.
Dann ist $(u_{j_{k}})$ glm. in $L^\infty$ beschränkt. Also gibt es ein $C> 0$ mit 
$$
|u_{j_{k}}(x)|\leq C
$$
für fast alle $x$ und alle $k$
Für $R>C$ gilt daher $\phi_{R}(u_{j_{k}})u_{j_{k}}=u_{j_{k}}$ und der Term ist identisch 0.

In allen Fällen gilt 
$$
\lim_{ R \to \infty } \sup_{k}|\int_{\Omega}g\cdot(u_{j_{k}}-\phi_{R}(u_{j_{k}})u_{j_{k}})\,dx| = 0 
$$
beziehungsweise
$$
\int_{\Omega}g\cdot \int_{\mathbb{R}^m}\phi_{R}(\lambda)\lambda\,d\nu_{x}(\lambda)\,dx\to \int_{\Omega}g\cdot u\,dx \text{ für }R\to \infty.
$$

Andererseits gilt
$$
\int_{\mathbb{R}^m}\phi_{R}(\lambda)\lambda\,d\nu_{x}(\lambda)\to \int_{\mathbb{R}^m}\lambda d\nu_{x}(\lambda)
$$
für fast alle $x$ (wegen monotoner Konvergenz für den Betrag von lambda im wesentlichen bzw. glm. Beschränktheit bei $p= \infty$, da hat das Young-Maß auch dementsprechend beschränkten Träger) 
Insgesamt aus dominierter Konvergenz (Hölder bzw. glm. Beschränktheit bei $p= \infty$, man mach das so ähnlich wie oben)
$$
\int_{\Omega}g(x)\cdot \int_{\mathbb{R}^m}\phi_{R}(\lambda)\lambda\,d\nu_{x}(\lambda)\,dx\to \int_{\Omega}g(x)\int_{\mathbb{R}^m}\lambda d\nu_{x}(\lambda)\,dx.
$$

Jedenfalls erhalten wird das was wir wollen.