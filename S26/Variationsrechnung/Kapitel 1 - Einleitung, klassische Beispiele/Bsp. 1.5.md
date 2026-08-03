Für festes $0<\alpha< \frac{1}{2}$ sei 
$$
\mathcal{F}(u):=\int_{0}^1 (1+u'^2)^\alpha
dx \text{ auf } U=\{ u \in C^1[0,1]|u(0)=0, u(1)=1 \}.$$
Es ist $\forall u \in U :\mathcal{F}(u)>1$, da $u'\neq 0$ für $u \in U$.

Für 
$$
u_{n}(x):=\begin{cases}
0 \quad , 0 \leq x \leq 1- \frac{1}{n}\\ \\
n^2\left(  x-1+\frac{1}{n} \right)^2 \quad , 1-\frac{1}{n} \leq x \leq 1
\end{cases} \quad, n\in \mathbb{N}
$$
ist $u_{n} \in U$ und
$$
\mathcal{F}(u_{n})\leq \int_{0}^{1- /n}dx+\int^1_{1-\frac{1}{n}}(5n^2)^\alpha dx=1-\frac{1}{n}+5^\alpha n^{2\alpha-1} \overset{n\to \infty}{\to} 1
$$
verwende im zweiten Integral: $1+\overbrace{4n^4\left( x-1+ \frac{1}{n} \right)^2}^{=u_{n}^2}\leq 5n^2$.
Also ist $\mathrm{inf}_{u \in U}\mathcal{F}(u)=1$, das Infimum wird aber nicht angenommen.
Das Problem $\mathcal{F}(u)\to \mathrm{min}$ ist also in $U$ nicht lösbar!
Die Minimalfolge $(u_{n})_{n\in \mathbb{N}}$ ist nicht kompakt (in geeigneter Topologie).
Die Situation ist ähnlich wie beim Minimierungsproblem $f(x):=e^{-x}\to \mathrm{min}$ auf $\mathbb{R}$.
