Es gelten die Voraussetzungen zu Beginn der vorherigen Abschnitts. Ferner sei $f$ eine Carathéodory-Funktion, und es gelte für fast alle $x \in \Omega$, dass $u \mapsto f(x,u)$ monoton fallend ist.
Ferner gelte die Abschätzung
$$
|f(x,u)|\leq C|u|^{p-1}+h(x) \quad \text{ für } x \in \Omega, u \in \mathbb{R},
$$
wobei $C>0, h\in L^q(\Omega),q\in \mathbb{N}_{*}, 1<p< \frac{2n}{n-2}$, ($p<\infty$, falls $n\leq 2$) und $\frac{1}{q}+\frac{1}{p}=1$.
Dann existieren genau eine schwache Lösung und eine Konstante $C>0$, die nur von $A,c$ und $\Omega$ abhängen, so dass
$$
||u||_{H^1(\Omega)}\leq C(||g||_{H^1(\Omega)}+||h||_{L^q(\Omega)}).
$$
Daraus folgt insbesondere, dass die Lösung stetig von den Anfangsdaten abhängt.

##### Bemerkungen:
- $H^1(\Omega)\hookrightarrow L^q(\Omega)$ und $H^1(\Omega)\hookrightarrow \hookrightarrow L^p(\Omega)$ kompakt, da $p \in \mathbb{N}^*\cap\left( 1, \frac{2n}{n-2} \right)$.
- $F(v):=f(.,v)$, $F:H^1(\Omega)\to L^q(\Omega)$, da falls $v\in H^1(\Omega)$: $|F(v)|^q=|f(.,v(.))|^q \leq C|v|^{(p-1)q}+h(x)^q$, denn falls $\frac{1}{p}+\frac{1}{q}=1 \frac{\implies(p-1)}{p}=\frac{1}{q}\implies(p-1)q=p$ aber wir wissen, dass $H^1(\Omega)\hookrightarrow L^p(\Omega)$ sodass $v \in H^1(\Omega)\implies v\in L^p(\Omega)$, also $|F(v)|^q\leq C^q|v|^p+h^q \in L^1(\Omega)\implies F(v)\in L^q(\Omega)$.
- Wofür brauchen wir die Monotonie von $f(x,.)$? Da $f$ monoton im zweiten Argument gilt $(f(x,v)-f(x,u))(u-v)\leq 0$. Falls $u=0$: $f(x,v)v-f(x,0)v=(f(x,v)-f(x,0))(v-0)\leq 0 \implies \int_{\Omega}f(x,v)vdx\leq \int_{\Omega}f(x,0)vdx=\frac{\varepsilon}{2}\int v_{2}2dx+\frac{2}{\varepsilon}(f(x,0))^2dx.$. Aber wir hatten halt $\int_{\Omega}f(u,v)u_{v}dx$, also brauchen wir eine neue Strategie.

##### Beweis:
**Schritt 1:**
Wir definieren das Problem. Für $v \in L^p(\Omega), \sigma \in[0,1]$. Betrachte $u_{v,\sigma}\in H^1(\Omega)$ Lösung zu
$$
\begin{cases}
L(u_{v,\sigma})=\sigma f(x,v)\text{ in } \Omega \\
u_{v,\sigma}=\sigma g \text{ auf } \partial \Omega
\end{cases}
$$
Wir wissen, dass $S:L^p(\Omega)\times[0,1]\to L^p(\Omega)$, $(v,\sigma)\mapsto u_{v,\sigma}$ wohldefiniert ist (Theorie für lineare elliptische PDEs).
Außerdem ist für $v$ beliebig, $\sigma=0$ die eindeutige Lösung des Problems
$$
\begin{cases} L(u_{v,0})=0 \quad \text{ in } \Omega\\
u_{v,0}=0 \quad \text{ auf } \partial \Omega

\end{cases} 
$$
$u_{v,\sigma}=0=S(v,0)$.

**Schritt 2:**
Wir beweisen nun, dass $S$ stetig und kompakt ist.
Sei dafür $(v_{k})_{k} \subset L^p(\Omega)$ beschränkt und $(\sigma_{k})_{k}\subset[0,1]$.
Wir wollen zeigen, dass $(S(v_{k},\sigma_{k}))_{k}\subset L^p(\Omega)$ eine konvergente Teilfolge hat.

Dafür testen wir mit $u_{v_{k},\sigma_{k}}-\sigma_{k}g\in H_{0}^1(\Omega)$:
$$
\begin{align}
\int_{\Omega}\nabla u_{v_{k},\sigma_{k}}^TA \nabla(u_{v_{k},\sigma_{k}}-\sigma_{k}g)+ cu_{v_{k},\sigma_{k}}(u_{v_{k},\sigma_{k}}-\sigma_{k}g)dx &\stackrel{\text{Hölder, Young}}{\leq} \frac{\varepsilon}{2} ||u_{v_{k},\sigma_{k}}||^2_{L^p(\Omega)}+\frac{1}{2\varepsilon}||f(.,v_{k})||^2_{L^q(\Omega)}+\tilde{C}(A,c,g) \forall \varepsilon>0 \\
&\leq  \frac{\varepsilon}{2}||u_{v_{k},\sigma_{k}}-\sigma_{k}g||^2_{L^p(\Omega)}+ \frac{1}{2 \varepsilon}||\sigma_{k}g||^2_{L^p(\Omega)}+\frac{1}{2 \varepsilon}||F(v_{k})||^2_{L^q(\Omega)}+\tilde{C}(A,c,g)\forall\varepsilon>0 \\
&\stackrel{\varepsilon \text{ klein, (*) }}{\leq} \frac{\alpha}{4}||u_{v_{k},\sigma_{k}}||^2_{L^2(\Omega)}+ \hat{C}||v_{k}||_{L^p(\Omega)}^2+\tilde{\tilde{C}}(A,c,g)
\end{align}
$$

$(*):$ 
(1): 
$H^1(\Omega)\hookrightarrow L^p(\Omega)$ continously
(2):
$u_{v_{k},\sigma_{k}}-\sigma_{k}g \in H_{0}^1(\Omega)$
Poincarè liefert
$$ 
\begin{align}
||u_{v_{k},\sigma_{k}}-\sigma_{k}g||_{H^1(\Omega)}&\leq C_{2}||\nabla (u_{v_{k},\sigma_{k}}-\sigma_{k}g)||_{L^2(\Omega)} \\
&\leq \tilde{C_{1}}||\nabla u_{v_{k},\sigma_{k}}||_{L^2(\Omega)}+C_{3}
||\nabla g||_{L^2(\Omega)}\end{align}
$$

Unten bekommt man die Ungleichung für $||u_{v_{k},\sigma_{k}}||^2_{H^1(\Omega)}$ aus zweimaligem anwenden von Poincaré.
Also ist $(u_{v_{k},\sigma_{k}})$ beschränkt in $H^1(\Omega)\hookrightarrow\hookrightarrow L^p(\Omega)$ und hat damit eine stark konvergente Teilfolge in $L^p(\Omega)$.
Also ist $S$ kompakt.

Nun zeigen wir, dass $S$ stetig in $L^p(\Omega)$ ist.
Wir starten wieder bei der schwachen Formulierung:
$$
\int_{\Omega}\nabla u_{v_{k},\sigma_{k}}^T A\nabla(u_{v_{k},\sigma_{k}}-\sigma_{k}g)+cu_{v_{k},\sigma_{k}}(u_{v_{k},\sigma_{k}}-\sigma_{k}g)dx=\int_{\Omega}\sigma_{k}f(v_{k},x)(u_{v_{k},\sigma_{k}}-\sigma_{k}g)dx$$
Führen wir (durch Addieren und Subtrahieren) die Terme mit $g$ bzw. $\nabla g$ künstlich ein, erhalten wir durch ein paar Umformungen und wegen der Elliptizität des Problems:
$$
\begin{align}
\frac{\alpha}{2}\int_{\Omega}|\nabla u_{v_{k},\sigma_{k}}|^2dx & \stackrel{\sigma_{k}\in[0,1]}{\leq}C(A,g,\Omega)+\int_{\Omega}|f(x,v_{k})||u_{v_{k},\sigma_{k}}-\sigma_{k}g|dx \\
& \stackrel{\text{Hölder,Young}}{\leq} \frac{\varepsilon}{2}||u_{v_{k},\sigma_{k}}||^2_{L^p(\Omega)}+\frac{1}{2 \varepsilon}||f(.,v_{k})||^2_{L^q(\Omega)}+C \\
&\leq C_{1} \frac{\varepsilon}{2} ||u_{v_{k},\sigma_{k}}-\sigma_{k}g||_{L^p(\Omega)}^2 + \underbrace{C \frac{\varepsilon}{2}||g||_{L^p(\Omega)}^2}_{\text{konstant}} + \frac{1}{2\varepsilon}||f(.,v_{k})||_{L^q(\Omega)}^2 +C \\
& \stackrel{H^1 \hookrightarrow L^p}{\leq} \tilde{C_{1}} \frac{\varepsilon}{2} || \underbrace{u_{v_{k},\sigma_{k}}-\sigma_{k}g}_{\in H_{0}^1(\Omega)}||_{H^1(\Omega)}^2+ \frac{1}{2 \varepsilon}||f(.,v_{k})||_{L^q(\Omega)}^2 +C \\
& \stackrel{\text{Poincaré}}{\leq} \tilde{\tilde{C}} \frac{\varepsilon}{2}||\nabla u_{v_{k},\sigma_{k}}||_{L^2(\Omega)}^2 + \underbrace{\tilde{\tilde{C}} \frac{\varepsilon}{2}||\sigma_{k}g||_{L^2(\Omega)}^2}_{\text{konstant}}+ \frac{1}{2 \varepsilon}||f(.,v_{k})||_{L^q(\Omega)}^2 + C
\end{align}
$$
Da $\varepsilon > 0$ beliebig, können wir es so wählen, dass $\tilde{\tilde{C}} \frac{\varepsilon}{2}=\frac{\alpha}{4}$ und erhalten
$$
\begin{align}
\frac{\alpha}{4}\int_{\Omega}|\nabla u_{v_{k},\sigma_{k}}|^2dx &\leq C_{2}
||f(.,v_{k})||_{L^q(\Omega)}^2 +C \\
&\leq C_{2}\left( \underbrace{||C|v_{k}|^{p-1}+h(.)||_{L^q(\Omega)}}_{\leq \left( \int_{\Omega}C|v_{k}|^{(p-1)q}+|h|^qdx \right)^{1/q}} \right)^2+C \\
&\stackrel{1/p+1/q=1 \implies (p-1)q=p}\leq C_{2} \left( C\int_{\Omega}|v_{k}|^{p}dx + \int_{\Omega}h(x)^qdx \right)^{2/q} + C
\end{align}
$$
Wegen der Poincarè-Ungleichung gilt
$$
\begin{align}
||u_{v_{k},\sigma_{k}}||^2_{H^1(\Omega)}&\leq C ||u_{v_{k},\sigma_{k}-\sigma_{k}g}||_{H^1(\Omega)}^2+C(g,A) \\
&\leq C ||\nabla(u_{v_{k},\sigma_{k}}-\sigma_{k}g)||^2_{L^2(\Omega)}+C(g,A) \\
&\leq C||\nabla u_{v_{k},\sigma_{k}}||^2_{L^2(\Omega)}+C(g,A)
\end{align}
$$
Setzt man das oben ein, erhält man Beschränktheit der Folge.

Es gilt zunächst:
Falls $(v_{k})\subset L^p(\Omega)$ beschränkt ist, gilt wegen oben sofort $\text{sup}_{k}||u_{v_{k},\sigma_{k}}||\leq C< \infty$.
**ABER:** $H^1(\Omega) \hookrightarrow \hookrightarrow L^p(\Omega)$, daher existiert eine Teilfolge, sodass $(u_{v_{k_{n}},\sigma_{k_{s}}})_{n}$ stark in $L^p(\Omega)$ gegen ein $u^* \in L^p(\Omega)$ konvergiert.
Daher ist $S$ kompakt.

Extrahiert man eine weitere Teilfolge, so konvergiert diese gegen $u^*$ schwach in $H^1(\Omega)$.

Um zu beweisen, dass $S$ stetig ist, müssen wir zeigen, dass falls $v_{k}\to v$ stark in $L^p(\Omega)$ und $\sigma_{k}\to \sigma$ in $\mathbb{R}$, dann $S(v_{k},\sigma_{k})=u_{v_{k},\sigma_{k}}\to u_{v,\sigma}=S(v,\sigma)$ stark in $L^p(\Omega)$.

Wegen der Kompaktheit wissen wir, dass eine Teilfolge existiert, sodass
$$
\begin{cases}
u_{v_{k_{n}},\sigma_{k_{n}}}\to u^* \text{ stark in }L^p(\Omega) \\
u_{v_{k_{n}},\sigma_{k_{n}}} \rightharpoonup u^* \text{ schwach in } H^1(\Omega)
\end{cases}
$$
Was fehlt: $u^*=S(v,\lambda)$ und dann [[Uryson-Property]].

Per definitionem und wegen [[Lemma- Stetigkeit Caratheodory-Funktion]] gilt zunächst:
$$ \forall w \in H_{0}^1(\Omega):
\int_{\Omega}\underbrace{\nabla u_{v_{k_{n}},\sigma_{k_{n}}}}_{\to \nabla u^* \text{ in } L^2(\Omega)}^T \underbrace{A}_{\in L^\infty(\Omega)}\underbrace{\nabla w}_{\in L^2(\Omega)} + \underbrace{c}_{\in  L ^\infty} \underbrace {u_{v_{k_{n}},\sigma_{k_{n}}}}_{\in L^2(\Omega), \to u^* \in  L^2(\Omega)} \underbrace{w}_{\in L^2(\Omega)}dx=\underbrace{\sigma_{k_{n}}}_{\to \sigma}\int_{\Omega}\underbrace{f(x,v_{k_{n}})}_{\to f(x,v), \text{ wg. Lemma}}wdx
$$
Außerdem gilt ja für alle $n$
$$
u_{v_{k_{n}},\sigma_{k_{n}}}=\sigma_{k_{n}}g \quad \text{ auf } \partial \Omega.
$$
Wegen [[Aufgabe 3]] gilt dann, dass 
$$
u_{v,\sigma}=\sigma g \quad \text{ auf } \partial \Omega
$$
und wegen der jeweiligen $L^p$-Konvergenzen
$$
\forall w \in H_{0}^1(\Omega):\int_{\Omega}(\nabla u^*)^TA\nabla w+cu^*wdx=\sigma \int_{\Omega}f(x,v)wdx
$$
Damit ist $u^*$ schwache Lösung von
$$
\begin{cases}
Lu=\sigma f \quad \text{ in } \Omega \\
u=\sigma g \quad \text{ auf } \partial \Omega
\end{cases}
$$
Das ist ein lineares, elliptisches Problem und somit ist dessen Lösung eindeutig.
Also gilt $S(v,\sigma)=u^*$.
Aus [[Uryson-Property]] folgt dann, dass $S$ stetig ist.

**Schritt 3:**
Nun müssen wir zeigen, dass
$$
\{ v \in L^p(\Omega) \quad |\quad S(v,\sigma)= v \text{ für ein } \sigma \in [0,1]\}
$$
in $L^p(\Omega)$ beschränkt ist.
Wir wissen, dass die Lösung dieses Problems eh in $H^1(\Omega)$ liegt, also reicht es, zu überprüfen, dass
$$
\{ v \in H^1(\Omega) \quad |\quad S(v,\sigma)= v \text{ für ein } \sigma \in [0,1]\}
$$
in $L^p(\Omega)$ ist.
Sei also $v$ aus dieser Menge, also $v=S(v,\sigma)$ für ein $\sigma \in [0,1]$.
Wir testen die PDE mit $v-\sigma g\in H_{0}^1(\Omega)$.
$$
\int_{\Omega}\nabla v^TA\nabla(v-\sigma g)+cv(v-\sigma g)dx=\int_{\Omega}\sigma f(x,v)(v-\sigma g)dx
$$
Mit ähnlichen Umformungen wie oben erhalten wir
$$
\begin{align}
\frac{\alpha}{2}\int_{\Omega}|\nabla u|^2dx&\leq \sigma \int_{\Omega}f(x,v)(v-\sigma g)
dx+C(A,g,\Omega) \\
&=\sigma \int_{\Omega}\underbrace{(f(x,v)-f(x,\sigma g))(v-\sigma g)}_{\text{ f monoton:}\leq 0}dx +\sigma \int_{\Omega}f(x,\sigma g)(v-\sigma g)dx+C(A,g,\Omega) \\
&\leq \sigma \int_{\Omega}f(x,\sigma g)(v-\sigma g)dx+C(A,g,\Omega) \\
&=\sigma \int_{\Omega}f(x,\sigma g)vdx\underbrace{-\sigma \int_{\Omega}\sigma gf(x,\sigma g)dx}_{\text{konstant}}+C(A,g,\Omega) \\
&\stackrel{\text{Young, Hölder?}}{\leq} \frac{\varepsilon}{2}||v||^2_{L^p(\Omega)}+ \frac{1}{2 \varepsilon}||f(.,\sigma g)||_{L^q(\Omega)}^2+C(A,g,\Omega,f) \quad \text{ für } \varepsilon>0 \text{ bel.}
\end{align}
$$
Wir erhalten also
$$
\frac{\alpha}{2}||\nabla v||^2_{L^2(\Omega)}\leq \tilde{C}(A,f,g,\Omega) + \frac{1}{2 \varepsilon}||f(.,\sigma g)||^2_{L^q(\Omega)}+ \frac{\tilde{\tilde{C}}\varepsilon}{2}||\nabla v||^2_{L^2(\Omega)}
$$
Wähle $\varepsilon$ entsprechend, dann gilt
$$
\frac{\alpha}{4}||\nabla v||^2_{L^2(\Omega)}\leq C(A,f,g,\Omega).
$$
Wenden wir wieder den gleichen Trick mit Poincaré an, erhalten wir
$$
\begin{align}
||v||^2_{L^p(\Omega)}&\leq \hat{\hat{C}}||v-\sigma g||_{L^p(\Omega)}^2+\hat{C}(g,\Omega) \\
&\leq \bar{C}||v-\sigma g||_{H^1(\Omega)}^2+\hat{C}(g,\Omega) \\
&\leq \bar{\bar{C}}||\nabla (v-\sigma g)||^2_{L^2(\Omega)^2}+ \hat{C}(g,\Omega) \\
&\leq \bar{\bar{C}}||\nabla v||^2_{L^2(\Omega)}+ \hat{\bar{C}}(g,\Omega) \\
&\leq \tilde{\tilde{\tilde{C}}}(A,f,g,\Omega)
\end{align}
$$
Wegen [[Theorem 2.12 (Fixpunktsatz von Leray-Schauder)]] gibt es ein $u \in H^1(\Omega)$ sodass
$$
\begin{cases}
Lu=f(x,u) \quad \text{ in } \Omega \\
u=g \quad \text{ auf } \partial \Omega.
\end{cases}
$$
**Step 4:**
Es bleibt zu zeigen, dass die Lösung eindeutig ist.
Angenommen $u_{1},u_{2}$ sind Lösungen.
Dann erfüllt $u_{1}-u_{2}$ die folgende PDE
$$
\begin{cases}
L(u_{1}-u_{2})=f(x,u_{1})-f(x,u_{2}) \quad \text{ in } \Omega \\
u_{1}-u_{2}=0 \quad \text{ auf } \partial \Omega
\end{cases}
$$
Da $u_{1}-u_{2}\in H_{0}^1(\Omega)$, können wir damit testen. Wegen der Monotonie von $f$ gilt
$$
0\leq\int_{\Omega}\nabla(u_{1}-u_{2})^TA\nabla(u_{1}-u_{2})+c(u_{1}-u_{2})^2dx = \int_{\Omega}(f(x,u_{1})-f(x,u_{2}))(u_{1}-u_{2})dx\leq 0 
$$
Also 
$$\int_{\Omega}\nabla(u_{1}-u_{2})^TA\nabla(u_{1}-u_{2})+c(u_{1}-u_{2})^2dx=0$$
und wegen $u_{1}-u_{2} \in H_{0}^1(\Omega)$ folgt
$||\nabla(u_{1}-u_{2})||_{L^2(\Omega)}=0 \implies u_{1}-u_{2}$ ist konstant und daher $u_{1}-u_{2}=0$.