Sei $\Omega \subset \mathbb{R}^n,n\geq 1$ und sei $f$ eine Caratheodory-Funktion mit
$$|f(x,\lambda)|\leq c|\lambda|^r+h(x),\quad 1\leq q,qr\leq \infty; c>0; h \in L^q(\Omega), h\geq 0; \text{ f.ü. in } \Omega \text{ und } \forall \lambda \in \mathbb{R}$$
Defnieren wir $F(v):=f(.,v(.))$, so ist $F$ stetig von $L^{qr}(\Omega)\to L^q(\Omega)$.

##### Beweis:
Sei $(u_{k})\subset L^{qr}(\Omega)$, so, dass $u_{k}\to u$ stark in $L^{qr}(\Omega)$.
Wir müssen zeigen, dass $F(u_{k})\to F(u)$ stark in $L^q(\Omega)$.
Da $u_{k}\to u$ stark in $L^{qr}(\Omega)$, erhalten wir aus [[Konvergenz im Maß folgt Teilfolge konvergier ae]], dass
- $\exists(u_{k_{n}})\subset(u_{k})$ sodass $u_{k_{n}}\to u$ fast überall in $\Omega$.
- $\exists g \in L^r(\Omega)$ sodass $|u_{k_{n}}(x)|\leq g(x)$ für fast alle $x \in \Omega$.
Es gilt 
$$
\begin{align}
|F(u_{k_{n}})|^q=|f(x,u_{k_{n}}(x))|^q\leq(c|u_{k_{n}}(x)^r+h(x)^q)\leq c'(|u_{k_{n}}(x)|^{qr}+h(x)^q) \leq g(x)^{qr}+h(x)^q
\end{align}
$$
Aus dominierter Konvergenz folgt
$$
\int_{\Omega}|F(u_{k_{n}})|^qdx \to \int_{\Omega}|F(u)|^qdx
$$
also stark in $L^q(\Omega)$.
