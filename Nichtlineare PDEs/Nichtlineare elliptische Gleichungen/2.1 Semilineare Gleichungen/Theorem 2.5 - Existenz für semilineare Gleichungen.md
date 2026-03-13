Es gelten die Voraussetzungen von Beginn dieses Abschnitts. Ferner sei $f$ eine Carathéodory-Funktion mit
$$
|f(x,u)|\leq h(x) \quad \text{ für } x \in \Omega,u\in \mathbb{R}, \text{wobei }h\in L^q(\Omega),q\in N_{*}.
$$
Dann existieren eine schwache Lösung $u\in H^1(\Omega)$ von unserem Problem und eine Konstante $C>0$, die nur von $A,c$ und $\Omega$ abhängt, sodass
$$
||u||_{H^1(\Omega)}\leq C(||g||_{H^1(\Omega)}+||h||_{L^q(\Omega)}).
$$
#### Bemerkung: 
Keine eindeutige Lösung, die geht wegen dem Fixpunkt verloren.
#### Beweis
Wir erinnern an: ![[Theorem 1.4. Einbettungssatz von Sobolev|Theorem 1.4.: Einbettungssatz von Sobolev]]
Der Beweis gliedert sich in mehrere Schritte.
Für Testfunktionen aus $H_{0}^1(\Omega)$ erhalten wir die schwache Formulierung
$$
\begin{cases}
\forall v \in H_{0}^1(\Omega):\int_{\Omega}(\nabla u^TA \nabla v+cuv)dx=\int_{\Omega}f(x,u)vdx \\
u=g \text{ auf } \partial \Omega
\end{cases}
$$
Wenn $u \in H^1(\Omega)$, dann ist die L.H.S. wohldefiniert.
Ob die R.H.S. wohldefiniert ist, ist zunächst nicht klar.
Zu zeigen wäre:
- $f(x,u(x))v$ ist messbar.
- $f(x,u(x))v \in L^1(\Omega)$.
Ersteres ist Übungsaufgabe.
![[cara1.png]]
![[cara2 1.png]]

Zweiteres gilt, da
$$
\int_{\Omega}|f(x,u(x))||v(x)|dx \leq \int_{\Omega}h(x)|v(x)|dx
$$
mit $h \in L^q(x)$, $q \in N_{*}$ und $v \in H_{0}^1(\Omega)$. Da $q \in N_{*}$ existiert ein $p \in N^*$ sodass der $H^1$ stetig in $L^p(\Omega)$ einbettet, d.h. man kann schreiben $v \in L^p(\Omega)$.
Nach Hölder folgt dann $h(x)|v(x)|\in L^1(\Omega)$.
##### Schritt 1: Definition des Fixpunktoperators
Sei $v \in K= \{L^2(\Omega):||v||_{H^1(\Omega)}\leq M\}$, wobei wir $M>0$ später definieren.

**Konvex**
Seien $u_{1},u_{2}\in K, t\in(0,1).$ Dann ist auch $u_{1}t+u_{2}(1-t)\in H^1(\Omega)$.
$$
||u_{1}t+u_{2}(1-t)||\leq t||u_{1}||+(1-t)||u_{2}||\leq M
$$
$\implies u_{1}t+u_{2}(1-t)\in M.$

**Kompakt** (in $L^2(\Omega)$), weil sonst wärs auch nicht kompakt.
Wählen wir eine Folge $(u_{k})\subset K$, so müssen wir erstens zeigen, dass sie eine konvergente Teilfolge hat und dass dieser Grenzwert in $K$ liegt.

Aus der kompakten Einbettung $H^1(\Omega)\hookrightarrow L^2(\Omega)$ folgt, dass eine Teilfolge $(u_{k'})$ von $(u_{k})$ existiert mit $u_{k'}\to u^*$ stark in $L^2(\Omega)$ für $k' \to \infty$.
$K$ ist reflexiv und $(u_{k'})$ beschränkt in $H^1(\Omega)$, d.h. es gibt wiederum eine Teilfolge $(u_{k''})$, sodass $u_{k''}\rightharpoonup u^* \in H^1(\Omega)$.
Die Grenzfunktion $u$ liegt in $K$, da nach [[Proposition 1.12. Eigenschaften schwacher Konvergenz]] (bzw. dem Lemma von Mazur) gilt:
$$
||u||_{H^1(\Omega)}\leq \mathrm{lim inf}_{k'\to \infty}||u_{k'}||_{H^(\Omega)} \leq M.
$$
Also ist $K$ kompakt.
Nun wollen wir die Wohldefiniertheit des Lösungsoperators überprüfen.
Sei $u \in H^1(\Omega)$ die eindeutig bestimmte Lösung des *linearen* Randwertproblems
$$
L(u)=f(x,v) \quad \text{ in } \Omega,\quad u=g \quad \text{ auf } \partial \Omega.
$$
Dieses Problem ist lösbar (etwa nach dem Lemma von Lex-Milgram), wenn die rechte Seite in $H^{-1}(\Omega)$ liegt. 

Dies ist der Fall, denn nach Voraussetzung gilt $|f(x,v(x))|\leq h(x)\in L^q(\Omega) \hookrightarrow H^{-1}(\Omega)$.
Genauer: Wir müssen zeigen $\mathrm{sup}_{\varphi \in H_{0}^1(\Omega),||\varphi||_{H_{0}^1(\Omega)}\leq 1} | \langle f(.,v(.)),\varphi \rangle_{H^{-1}(\Omega),H_{0}^1(\Omega)}|\leq C$
Also das Integral über das Produkt mit einer beliebigen Testfunktion mit Norm $1$ soll gleichmäßig in $\varphi$ beschränkt sein.
Wir wissen schon, dass $v\in K$ also insbesondere in $H^1(\Omega)$, damit ist $f(x,v(x))\in L^q(\Omega)$.
Da $\varphi \in H_{0}^1(\Omega)$ ist $\varphi \in L^{q^*}(\Omega)$ mit $q^*$ derart, dass $\frac{1}{q}+\frac{1}{q^*}=1$.
Nach Hölder ist $S:K\to H^1(\Omega)$ wohldefiniert.
Es bleiben zu zeigen, dass $S$ eine Selbstabbildung (d.h. $S:K\to K$) und stetig ist.

##### Schritt 2: S ist eine Selbstabbildung (für geeignetes M)
Wir zeigen, dass $S(K)  \subset K.$ Dies ist der wichtigste Schritt im Beweis.
Sei $u=S(v)\in S(K)$. Wir verwenden die Testfunktion $u-g\in H_{0}^1(\Omega)$ in der schwachen Formulierung, da wir eigentlich gerne mit $u$ testen würden aber $u \not\in H_{0}^1(\Omega)$:
$$
\int_{\Omega}(\nabla u^TA \nabla(u-g)+cu(u-g))dx=\int_{\Omega}f(x,v)(u-g)dx.
$$
Wir ergänzen, damit wir schlussendlich $||u-g||$ erhalten und schätzen die linke Seite ab, indem wir die Elliptizität von A und die Youngsche Ungleichung verwenden. Uns ist hierbei egal, ob die Konstanten vor den Termen, die nicht von $u$ abhängen groß sind, weil wir die dann mit der Wahl von $M$ absorbieren. Beim zweiten Term, wo die Young'sche Ungleichung anwenden, verwenden wir $c(x)=\sqrt{ c(x) }\sqrt{ c(x) }$.
$$
\begin{align}
\int_{\Omega}(\nabla u^TA \nabla (u-g)+cu(u-g))dx &= \int_{\Omega}(\nabla (u-g)^TA \nabla (u-g)+\nabla g^TA \nabla(u-g)+c(u-g)^2+cg(u-g))dx \\
&\geq \int_{\Omega}\left(   \alpha|\nabla (u-g)|^2-\frac{\alpha}{2} |\nabla(u-g)|^2 -  \frac{|A|^2}{2\alpha}|\nabla g|^2+c(u-g)^2-\frac{c}{2}(u-g)^2-\frac{c}{2}g^2 \right)dx \\
&\geq \frac{\alpha}{2} ||\nabla(u-g)^2||^2_{L^2(\Omega)}-\frac{1}{2\alpha}||A||_{L^\infty(\Omega)}^2||\nabla g||^2_{L^2(\Omega)}-\frac{1}{2}||c||_{L^\infty(\Omega)}||g||^2_{L^2(\Omega)}.

\end{align}
$$
In der letzten Ungleichung lassen wir den Term $\int_{\Omega} \frac{c}{2}(u-g)^2dx$ einfach weg, da der Integrand nicht negativ ist und sonst nichts bringt.

Für die Abschätzung der rechten Seite verwenden wir die Voraussetzung an $f$ und die Young-Ungleichung, wobei wir wieder das $\varepsilon$ bei den Termen, die von $u$ abhängen im Zähler haben, damit die Konstante klein ist, während sie uns bei dem $h$-Term egal ist, weil diese Konstante sowieso $M$ frisst:
$$
\begin{align}
\int_{\Omega}f(x,v)(u-g)dx &\leq \int_{\Omega}h|u-g|dx
\leq||h||_{L^q(\Omega)}||u-g||_{L^p(\Omega)} \\
&\leq \frac{\varepsilon}{2}||u-g||^2_{L^p(\Omega)}+\frac{1}{2\varepsilon}||h||^2_{L^q(\Omega)},
\end{align}
$$
Wegen $1/p +1/q = 1$  gilt $p \in N^*$, und wir schließen $H^1(\Omega)\hookrightarrow  L^p(\Omega)$. Außerdem folgt aus der Einbettung sowie der Poincaré-Ungleichung, dass
$$
||u-g||_{L^p(\Omega)}\leq C_{1}||u-g||_{H^1(\Omega)}\leq C_{2} ||\nabla(u-g)||_{L^2(\Omega)}
$$
mit gewissen Konstante $C_{1},C_{2}$. 
Wählen wir uns nun $\varepsilon>0$ hinreichend klein (z.B. $\varepsilon=\frac{\alpha}{2C_{2}^2}$), so können wir den Term $\frac{\varepsilon}{2}||u-g||^2_{L^p(\Omega)}\leq \frac{\alpha}{4}||\nabla(u-g)||_{L^2(\Omega)}^2$ durch den entsprechenden Ausdruck absorbieren. Fassen wir also die Abschätzungen beider Seiten zusammen, erhalten wir
$$
\frac{\alpha}{4}||\nabla(u-g)||_{L ^2(\Omega)}^2\leq \frac{1}{2\alpha}||A||_{L^\infty(\Omega)}^2||\nabla g||^2_{L^2(\Omega)}+\frac{1}{2}||c||_{L^\infty(\Omega)}||g||_{L^2(\Omega)^2}+\frac{1}{2\varepsilon}||h||_{L^q(\Omega)^2}=:M_{0}^2.
$$
Wir erhalten also $\int_{\Omega}|\nabla(u-g)|^2dx\leq M_{0}$, $M_{0}\geq 0$.
Mittels Dreiecksungleichung und Poincaré-Ungleichung schreiben wir
$$ \begin{align}
||u||&\leq||u-g||_{H^1(\Omega)}+||g||_{H^1(\Omega)} \\
&\leq C_{3}||\nabla(u-g)||_{L^2(\Omega)}+||g||_{H^1(\Omega)} \\
&\leq C_{3}M_{0}+||g||_{H^1(\Omega)}=:M,
\end{align}
$$
wobei die ganzen anderen Konstanten an keiner Stelle von der Wahl von $M$ abhängen.

##### Schritt 3: S ist stetig in $L^2$
Wir müssen zeigen, dass für $(v_{k})\subset K$ mit $v_{k}\to v$ stark in $L^2(\Omega)\implies u_{v_{k}}:=S(v_{k})\to S(v)$ stark in $L^2(\Omega)$.


> [!NOTE] Strategie
> 
> -  Zeigen, dass  $(S(v_{k}))$ präkompakt in $L^2(\Omega)$ ist und eine Teilfolge $(S(v_{k_{n}}))$ existiert, die stark in $L^2(\Omega)$ zu einem Grenzwert $\phi \in L^(\Omega)$ konvergiert.
> - $\phi=S(v)$
> - (Gratis) Da man aus jeder Teilfolge von  $(v_{k})$ eine Teil-Teilfolge $(v_{k_{n_{j}}})$ extrahieren kann,  sodass $S(v_{n_{k_{j}}})\to S(v)$ folgt ([[Uryson-Property]]): $S(v_{k})\to S(v)$.

Analog zu zu Schritt 1 finden wir $(u_{v_{k_{n}}})\subset(u_{v_{k}})\subset K$ sodass
$$
\begin{cases}
u_{v_{k_{n}}}\to u^* \text{ schwach in } H^1(\Omega) \\
u_{v_{k_{n}}} \to u^* \text{ stark in } L^(\Omega)
\end{cases}
$$
Wir müssen zeigen, dass $u^*=S(v)$.
Wir wissen, dass $\forall w \in H_{0}^1(\Omega):\int_{\Omega}[\nabla u_{v_{k}}^TA\nabla w+cu_{v_{k}}w]dx=\int_{\Omega}f(x,v_{k})wdx$.
Der Integrand ist in $L^2$ und konvergiert für $k \to \infty$ gegen $\int_{\Omega}\nabla u^*A\nabla w+cu^*wdx$

> [!NOTE] Anmerkung:
> 
> **Falls** $\int_{\Omega}f(x,v_{k})wdx\to \int_{\Omega}f(x,v)wdx$ erhalten wir
> $$
> \forall w\in H_{0}^1(\Omega):\int_{\Omega}\nabla u^*A\nabla +cu^*wdx=\int_{\Omega}f(x,v)wdx
> $$
> **Falls** wir zusätzlich wüssten (Übung, wir verwenden, dass der Trace-Operator $\gamma:H^1(\Omega)\to L^2(\Omega)$ stark stetig in $L^2(\Omega)$ w.r.t. schwachen Konvergenz in $H^1(\Omega)$ ist.) , dass $u_{v_{k_{n}}}=g$ auf $\partial \Omega$ $\implies u^*=g$ auf $\partial \Omega$, wüssten wir $S(v)=u^*$
> und wären somit fertig
> ![[Pasted image 20260313122614.png]]
>

Die erste Aussage erhalten wir aus [[Lemma- Stetigkeit Caratheodory-Funktion]]:
- Wähle $q$ gleich wie im Statement des Satzes, $q \in \mathbb{N}_{*}$.
- Wähle $r$ sodass $H^1(\Omega)\hookrightarrow L^{qr}(\Omega)$ kompakt.
- Wähle $c=0$.
- Da $v_{k}\to v$ schwach in $H^1(\Omega)$ folgt aus der Kompaktheit der Einbettung, dass es eine Teilfolge $(v_{k_{n}})$ gibt, die $v_{k_{n}}\to v$ stark in $L^{qr}(\Omega)$.
- Wegen dem Lemma folgt $F(v_{k_{n}})\to F(v)$ stark in $L^q(\Omega)$.
- Daher konvergiert $f(x,v_{k_{n}}(x))\to f(x,v(x))$ stark in $L^q(\Omega)$.
- Aber $w \in H^1_{0}(\Omega)\hookrightarrow L^{q^*}(\Omega)$, also $w \in L^{q^*}(\Omega)$.
- Daher konvergiert $\forall w \in H_{0}^1(\Omega):\int_{\Omega}f(x,v_{k_{n}})wdx\to \int_{\Omega}f(x,v)wdx$ stark in $L^q(\Omega)$.
Damit erfüllt $u$ $\int_{\Omega}\nabla uA\nabla w+cuwdx=\int_{\Omega}f(x,v)wdx$ und löst somit 
$$
\begin{cases}
L(u)=f(x,v(x)) \text{ in } \Omega, \\
u=g \text{ auf } \partial \Omega
\end{cases}
$$
Da das Problem eindeutig lösbar ist, folgt $u=S(v)$.
Damit ist, wie in der Strategie beschrieben, $S$ stetig.

###### Schritt 4:
Wir können [[Theorem 2.3 - Fixpunktsatz von Schauder]] anwenden und erhalten die Existenz von 
$u \in K$ sodass $S(u)=u$, d.h. $u \in H^1(\Omega)$ löst unser Problem.







