
Im Wesentlichen stellt man eine Bilanzgleichung zwischen Deformationsenergie, Arbeit der Volumskraft und Arbeit der Oberflächenkraft auf und versucht diese zu minimieren.
Bei hypererlastischen Materialieen kann man die Deformationsenergie so beschreiben
$$
E_{\mathrm{def}}=\int_{\Omega} W(C(x))\, dx, 
$$
wobei $W:\{A\in \mathbb{R}^{d\times d}|A=A^T\}\to \mathbb{R}$ die Energiedichte ist. Falls das Material inhomogen ist, kann $W$ auch explizit von $x$ abhängen. Oft nimmt man an, dass das Material isotrop ist.
Dieser Ansatz führt zu folgender Formulierung für die Gesamtenergie
$$
E_{\mathrm{ges}}=\underbrace{\int_{\Omega}W(C(u(x)))\mathrm{ d}x}_{\text{Deformationsenergie}} 
-\underbrace{\int_{\Omega}f\cdot u\mathrm{ d}x}_{\text{Arbeit der Volumskraft}}  
-\underbrace{\int_{\Gamma_{\mathrm{N}}}b \cdot u \mathrm{ d}S}_{\text{Arbeit der Oberflächenkraft}}
$$
Wir wollen nun eine Gleichung für die gesuchte Verschiebung $u$ durch die Minimierung der Gesamtenergie finden.
Außerdem soll die Verschiebung die Randbedingung $u|_{\Gamma_\mathrm{D}}=0$ erfüllen.

Nullsetzen der Richtungsableitungen und etwas Arbeit ([[Herleitung der Euler-Lagrange-Gleichungen]]) führt zu den folgenden Gleichungen (Euler-Lagrange Gleichungen von $E_{\mathrm{ges}}$), wobei $\Sigma:=2 \frac{\mathrm{d}W}{\mathrm{d}C}(C)$ den 2. Piola-Kirchhoff'schen Spannungstensor bezeichnet (vgl. [[Satz 2.6.2]]):
$$
\begin{cases}
-\mathrm{div}\left( \left( \frac{\partial u}{\partial x}+\mathrm{I} \right)\cdot \Sigma \right) = f \text{ in } \Omega \\
(\frac{\partial u}{\partial x}+\mathrm{I})\cdot \Sigma \cdot n =b \text{ auf } \Gamma_{\mathrm{N}}
\end{cases}
$$
Außerdem soll noch gelten $u|_{\Gamma_\mathrm{D}}=0$.
Dieses System gilt es zu lösen.