Für $s \in (0,1)$ definieren wir:

**Def.:**
$$
W^{s,p}(\Omega)=\left\{  u \in L^p(\Omega)\quad|\quad \frac{|u(x)-u(y)|}{|x-y|^{n/p+s}} \in L^p(\Omega) \right\}
$$
$$
||u||_{W^{s,p}(\Omega)}:=\left( \int_{\Omega}|u|^pdx+\int_{\Omega}\int_{\Omega} (\frac{|u(x)-u(y)|}{|x-y|^{n/p+s}})^pdxdy\right)^{1/p}
$$

Wir können zeigen, dass für $0<s\leq s'<1$ gilt $W^{s',p}(\Omega)\hookrightarrow W^{s,p}(\Omega)$ stetig:

**Proposition 2.1:**
$p \in [1,+\infty)$ und $0<s\leq s'<1$. Sei $\Omega$ offen in $\mathbb{R}^n$ und $u:\Omega \to \mathbb{R}$ eine messbare Funktion.
Dann gilt $||u||_{W^{s,p}(\Omega)}\leq C||u||_{W^{s,p}(\Omega)}$ für eine geeignete Konstante $C = C(n,s,p)\geq 1$.
Insbesondere gilt $W^{s',p}(\Omega)\subset W^{s,p}(\Omega)$.

*Beweis:*
Es gilt
$$
\int_{\Omega}\int_{\Omega\cap \{ |x-y|\geq 1 \}} \frac{|u(x)|^p}{|x-y|^{n+sp}}dxdy\leq \int_{\Omega}\left( \int_{|z|\geq 1} \frac{1}{|z|^{n+sp}}dz\right)|u(x)|^pdx
$$
wobei wir verwendet haben, dass der Kern $\frac{1}{|z|^{n+sp}}$ integrierbar über dieser Menge ist, da $n+sp>n$.
Es folgt, dass
$$
\begin{align}
\int_{\Omega}\int_{\{ |x-y|\geq 1 \}}\frac{|u(x)-u(y)|^p}{|x-y|^{n+sp}}dxdy&\leq 
\int_{\Omega}\int_{\{ |x-y|\geq 1 \}}\frac{(|u(x)|+|u(y)|)^p}{|x-y|^{n+sp}}dxdy \\
&\leq
2^{p-1}\int_{\Omega}\int_{\{ |x-y|\geq 1 \}}\frac{|u(x)|^p+|u(y)|^p}{|x-y|^{n+sp}}dxdy \\
&=2^{p-1}\left(2 \int_{\Omega}\int_{\Omega\cap \{ |x-y|\geq 1 \}} \frac{|u(x)|^p}{|x-y|^{n+sp}}dxdy \right) \\

&\leq 2^p C(n,s,p)||u||^p_{L^p(\Omega)}
\end{align}
$$
Andererseits gilt (für den Rest der Menge, über die integriert wird):
$$
\int_{\Omega}\int_{\Omega\cap \{ |x-y |<1\}}\frac{|u(x)-u(y)|^p}{|x-y|^{n+sp}}dxdy \stackrel{s'\geq s}{\leq} \int_{\Omega}\int_{\Omega\cap \{ |x-y|<1 \}}\frac{|u(x)-u(y)|^p}{|x-y|^{n+s'p}}dxdy
$$
Wir kombinieren wir diese Abschätzungen
$$
\begin{align}
\int_{\Omega}\int_{\Omega}\frac{|u(x)-u(y)|^p}{|x-y|^{n+sp}}dxdy &=\int_{\Omega}\int_{\{ |x-y|\geq 1 \}}\frac{|u(x)-u(y)|^p}{|x-y|^{n+sp}}dxdy + \int_{\Omega}\int_{\Omega\cap \{ |x-y |<1\}}\frac{|u(x)-u(y)|^p}{|x-y|^{n+sp}}dxdy  \\
&\leq 2^p C(n,s,p)||u||_{L^p(\Omega)}^p + \int_{\Omega}\int_{\Omega}\frac{|u(x)-u(y)|^p}{|x-y|^{n+s'p}}
\end{align}
$$
Schlussendlich erhalten wir
$$
\begin{align}
||u||^p_{W^{s,p}(\Omega)} &\leq (2^pC(n,s,p)+1)||u||_{L^p(\Omega)}^p+\int_{\Omega}\int_{\Omega}\frac{|u(x)-u(y)|^p}{|x-y|^{n+s'p}}dxdy \\
&\leq C(n,s,p)||u||^p_{W^{s',p}(\Omega)}
\end{align}
$$
wenn man $C(n,s,p)$ umbenennt.

Dieses Resultat gilt (unter zusätzlichen Annahmen an $\partial \Omega$) auch im Grenzfall, also wenn $s'=1$.

**Proposition 2.2:**
