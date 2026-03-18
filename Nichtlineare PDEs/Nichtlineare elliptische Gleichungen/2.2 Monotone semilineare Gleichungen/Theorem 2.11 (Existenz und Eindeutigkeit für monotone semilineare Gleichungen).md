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
