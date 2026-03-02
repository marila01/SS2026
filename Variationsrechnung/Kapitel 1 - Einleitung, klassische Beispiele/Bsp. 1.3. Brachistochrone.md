(Bernoulli, 1696; brachistos ($\beta \rho \alpha \chi \iota \sigma \tau o\sigma$) = kürzeste, chronos ($\chi \rho o \nu o \sigma$) = Zeit)

**Aufgabe:** Finde Kurve $u=u(x)$ zwischen Punkten $A=(0,0)$ und $B=(b_{1},b_{2})$ mit $b_{1}>0, b_{2}>0$ sodass ein Körper in dem konstanten Schwerefeld $F=(g,0), g>0$ reibunsfrei, *möglichst schnell* von $A$ nach $B$ kommt - bei Anfangsgeschwindigkeit $0$.

**Lösung:** Zykloidbögen (Radkurve), obwohl längerer Weg als Verbindungsgerade.
![[Pasted image 20260301153537.png]]
**Formale Herleitung der mathematischen Formulierung**
$m$ ... Masse des Körpers
$(x(t),u(t))$ ... Position des Körpers zur Zeit $t$
$s(t)$ ... Zurückgelegter Weg (Bogenlänge)

2.Newton'sches Gesetz (in tangentialer Richtung), d.h. Masse $\times$ Beschleunigung $=$ Kraft:
$$
m\frac{\mathrm{d}^2s}{\mathrm{d}t^2}=F\cdot e_t(x)=m\frac{g}{\sqrt{ 1+u'^2 }},
$$
$e_{t}(x)=\frac{1}{\sqrt{1+u'^2 }}\begin{pmatrix}1\\ u'\end{pmatrix}$ ... Einheitstangentialvektor an Kurve

**Gesucht:** $t(x)$ bzw. $x(t)$, $\frac{\mathrm{d}x}{\mathrm{d}t}=$ vertikale Geschwindigkeitskomponente.

Bogenlängenelement: $\sqrt{ 1+u'^2 }\mathrm{d}x=\mathrm{d}s\implies \sqrt{ 1+u'^2 }=\frac{\mathrm{d}s}{\mathrm{d}x}=\frac{\mathrm{d}s}{\mathrm{d}t}\frac{\mathrm{d}t}{\mathrm{d}x}$.
$$
\implies g = \frac{\mathrm{d}^2s}{\mathrm{d}t^2} \sqrt{ 1+u'^2 }=\frac{\mathrm{d}^2s}{\mathrm{d}t^2}\frac{\mathrm{d}s}{\mathrm{d}t}\frac{\mathrm{d}t}{\mathrm{d}x}= \frac{1}{2}[\frac{\mathrm{d}}{\mathrm{d}t}(\frac{\mathrm{d}s}{\mathrm{d}t})^2]\frac{\mathrm{d}t}{\mathrm{d}x}
$$
$$
\implies g \frac{dx}{dt}=\sqrt{ \frac{1+u'^2}{2gx} } \quad | \int_{0}^{b_{1}}\dots dx
$$
$$
\text{Durchlaufzeit } = \frac{\int_{0}^{b_{1}}1}{\sqrt{ 2gx }}\sqrt{ 1+u'^2 }dx
$$
**Mathematische Problemstellung:**
Definiere die Funktionenmenge $U:=\{u \in C^1[0,b_{1}]|u(0)=0, u(b_{1})=b_{2} \}$ und das Funktional
$$
\mathcal{F}:U\to \mathbb{R}, \mathcal{F} := \int_{0}^{b_{1}} \frac{1}{\sqrt{ 2gx }}\sqrt{ 1+u'^2 }dx
$$
Finde $u_{0}\in U$, so dass $\mathcal{F}(u_{0})$ minimal wird.

**Offene Fragen:**
- Ist $U$ eine/die geeignete Menge?
- Gibt es ein Minimum von $\mathcal{F}$ auf $U$? Wenn ja, ist es eindeutig?
- Wie findet man es?