Eine Körperkraft heißt **dead load**, wenn die Dichte $f$ in der Referenzkonfiguration unabhängig von der Deformation ist.

Das ist z.B. beim Gravitationsfeld der Fall ($f(x)=-\mathrm{g}\rho(x)e_{3}$)

Eine Oberflächenkraft heißt **dead load**, wenn die Dichte $g$ in der Referenzkonfiguration nicht von der Deformation abhängt.

Ein einfaches Beispiel dafür wäre $g(x)=0$, dh ein Teil vom Rand ist fixiert und $\Gamma_{1}^\Phi$ ist frei von externen Sachen.

Oft nimmt man an, dass alle Kräfte dead loads sind, weil es mathematisch einfacher wird.
Jedoch ist dies in der Realität selten der Fall, z.B. wenn man irgendwo draufdrückt.
In Ciralet p80 wird das genauer durchgenommen.
Jedenfalls motiviert dies die Annahme, die wir in Zukunft immer treffen werden:

*Ab nun sind alle Kräfte entweder dead loads oder haben die folgende Form*
$$
\begin{align}
f(x)=\hat{f}(x,\Phi(x)), x \in \Omega,\\ \\
g(x)=\hat{g}(x,\nabla \Phi(x)), x \in \Gamma_{1}
\end{align}
$$
*für gegebenes $\hat{f}:\Omega \times \mathbb{R}^3\to \mathbb{R}^3$ bzw. $\hat{g}:\Gamma_{1}\times \mathbb{M}_{+}^3\to \mathbb{R}^3$* 

Eine Ausnahme, die nicht dieser Annahme genügt, ist das Ballon Problem, wo die Oberflächenkraft nicht lokal ist.

Eine Körperkraft ist **konservativ**, wenn das Integral $\int_{\Omega}f(x)\cdot \theta(x)\mathrm{d}x=\int \hat{f}(x,\Phi (x))\cdot \theta(x)\mathrm{d}x$, das im principle of virtual work in der Referenzkonfiguration (vgl. [[Satz 2.6.1]],[[Satz 2.6.2]]) vorkommt, auch als Gâteaux Ableitung 
$F'(\Phi)\theta=\int_{\Omega}\hat{f}(x,\Phi (x))\mathrm{d}x$ eines Funktionals $F:\{ \psi:\bar{\Omega}\to \mathbb{R}^3 \}\to \mathbb{R}, F(\psi)=\int_{\Omega}\hat{F}(x,\psi(x))\mathrm{d}x$, $\hat{F}:\Omega \times \mathbb{R}^3\to \mathbb{R}$ Potential, geschrieben werden kann.

Eine Kraft, die eine dead load ist, ist konservativ $\hat{F}(x,\eta)=f(x)\cdot \eta$.

Generell ist eine Dichte der Form $f(x)=\hat{f}(x,\Phi(x))$ konservatv, falls $\forall x \in \Omega,\eta \in \mathbb{R}^3:\hat{f}(x,\eta)=grad_{\eta}\hat{F}(x,\eta)$.

Z.B. die Zentrifugalkraft ist konservativ.

Ähnlich dazu nennt man eine Oberflächenkraft mit Dichte $g$ **konservativ**, wenn das Inegral, das im principle of virtual work in der Referenzkonfiguration geschrieben werden kann als Gâteaux-Ableitung $G'(\Phi)\theta=\int_{\Gamma_{1}}\hat{g}(x,\nabla \Phi(x))\cdot \theta \mathrm{d}x$ eines Funktionals der Form $G:\{ \psi:\bar{\Omega}\to \mathbb{R}^3 \}\to \mathbb{R}, G(\psi)=\int_{\Gamma_{1}}\hat{G}(x,\psi(x),\nabla \psi(x))\mathrm{d}a$.
$\hat{G}:\Gamma_{1}\times \mathbb{R}^3\times \mathbb{M}^3_{+}\to \mathbb{R}$ heißt auch Potential der Oberflächenkraft.

Wieder ist eine Oberflächenkraft, die dead load ist, auch konservativ mit $\hat{G}(x,\eta,F)=g(x)\cdot \eta$.

Dann gibt es noch ein Beispiel dazu in Satz 2.7-1 aber ich find das bissi uninteressant.

Warum konservative Kräfte relevant sind, erkennt man spätestens in Kapitel 4, wenn man Hyperelastizität betrachtet.