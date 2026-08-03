Sei $Q=(0,1)^n$, $1\leq p\leq \infty$ und $u \in L^p(Q,\mathbb{R}^m)$.
Sei $(u_{j})_{j \in \mathbb{N}}\subset L^p(Q,\mathbb{R}^m)$ durch $u_{j}(x):=u(jx)$ gegeben, wobei $u$ $Q$-periodisch auf ganz $\mathbb{R}^n$ fortgesetzt wird.

Zeige, dass $(u_{j})_{j}$ das Young-Maß
$$
\langle \nu_{x},\phi\rangle=\int_{Q}\phi(u(y))\,dy, \quad \phi \in C_{0}(\mathbb{R}^m)
$$
erzeugt (dieses hängt nicht von $x$ ab und wird deshalb *homogen* genannt).

*Beweis:*
### 1.
Durch Substitution von $jx$ erhält man
$$
||u_{j}||^p_{L^p} = \int_{Q}|u(jx)|^p\,dx = \frac{1}{j^{n}}\int_{jQ}|u(y)|^p\,dy = \frac{j^n}{j^{n}}||u||_{L^p}^p
$$
Also ist $u_{j}$ beschränkt in $L^p$. 
Stärker sogar, es gilt
$$
\int_{\{ |u_{j}|>M \}}|u_{j}(x)|^p\,dx = \frac{1}{j^n}\int_{jQ}\mathbb{1}_{\{ |u(y)|>M \}}|u(y)|^p\,dy=\int_{Q}\mathbb{1}_{|u(y)|>M}|u(y)|^p\,dy
$$
weswegen das auch für das Supremum gilt,
Da $u \in L^p(Q)$ gilt trivialerweise, dass das Supremum für $M\to \infty$ gegen $0$ geht, daher ist die Folge straff.
Wegen dem Satz auf dem Aufgabenblatt gibt es eine weitere Teilfolge, die eben ein Young-Maß erzeugt, sodass  eben für alle $g \in L^1, \phi \in C_{0}(\mathbb{R}^m)$ und diese hat wiederum eine Teilfolge, die das macht
$$
\int_{\Omega}g(x)\phi(u_{j_{k_{\ell}}})\,dx\to \int_{\Omega}g(x)\langle\nu_{x},\phi\rangle\,dx.
$$


### 2.
Sei nun $\phi \in C_{0}(\mathbb{R}^m)$ und betrachte $f= \phi\circ u$.
Dann ist $f$ $Q$-periodisch und beschränkt.
Wir wollen $f(jx)\rightharpoonup^* \int_{Q}f(y)\,dy$ in $L^\infty(Q)$.
Sei daher zunächst $g \in C(\bar{Q})$, betrachte die Würfel $\frac{k+Q}{j}$ für $k \in \{ 0,\dots,j-1\}^n$.
Dann gilt
$$
\int_{Q}g(x)f(jx)dx =\sum_{k \in \{ 0,\dots,j-1 \}^n}\int_{\frac{k+Q}{j}}g(x)f(jx)dx
$$
Substituiere $y:=jx-k\in Q$, $x = \frac{k+y}{j}$ und wir erhalten einen Faktor $\frac{1}{j^n}$ davon, also
$$
\int_{Q}g(x)f(jx)dx = \frac{1}{j^n}\sum_{k \in \{ 0,\dots,j-1 \}^n}\int_{Q}g\left( \frac{k+y}{j} \right)f(y)dy = \int_{Q}\left( \frac{1}{j^n} \sum_{k \in \{ 0,\dots,j-1 \}^n}g\left( \frac{k+y}{j} \right)\right)f(y)dy
$$
Der eingeklammerte Ausdruck ist eine Riemannsumme für
$$
\int_{Q}g(x)dx,
$$
und da $g$ stetig, haben wir gleichmäßige Konvergenz in $y$ gegen das Integral, also insgesamt
$$
\int_{Q}g(x)f(jx)\,dx \to \int_{Q}\left( \int_{Q}g(x)\,dx \right)f(y)\,dy=\int_{\Omega}f(y)\,dy\cdot \int_{\Omega}g(x)\,dx
$$
Da $C(\bar{Q})$ dicht in $L^1(Q)$, gibt es eine Folge $g_{\ell}\in C(\bar{Q})$ mit $g_{\ell}\to g$ in $L^1(Q).$
Da $f \in L^\infty$ erhalten wir
$$
|\int_{Q}(g-g_{\ell})(x)f(jx)\,dx|\leq ||f||_{L^\infty}||g-g_{\ell}||_{L^1},
$$
genauso wie
$$
|\left( \int_{Q}(g-g_{\ell})(x)\,dx \right)\left( \int_{Q}f(y)\,dy \right)\leq ||f||_{L^\infty}||g-g_{\ell}||_{L^1},
$$
also erhalten wir Konvergenz für alle $g \in L^1$.
Das gilt auch für jede Teilfolge (einer Teilfolge) von $(u_{j})$ und daher erhalten wir wegen der Eindeutigkeit des Grenzwertes Gleichheit.