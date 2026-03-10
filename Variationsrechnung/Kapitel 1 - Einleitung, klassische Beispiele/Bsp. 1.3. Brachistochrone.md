(Bernoulli, 1696; brachistos ($\beta \rho \alpha \chi \iota \sigma \tau o\sigma$) = kürzeste, chronos ($\chi \rho o \nu o \sigma$) = Zeit)

**Aufgabe:** Finde Kurve $u=u(x)$ zwischen Punkten $A=(0,0)$ und $B=(b_{1},b_{2})$ mit $b_{1}>0, b_{2}>0$ sodass ein Körper in dem konstanten Schwerefeld $F=(g,0), g>0$ reibunsfrei, *möglichst schnell* von $A$ nach $B$ kommt - bei Anfangsgeschwindigkeit $0$.

**Lösung:** Zykloidbögen (Radkurve), obwohl längerer Weg als Verbindungsgerade.
![[Pasted image 20260301153537.png]]
**Formale Herleitung der mathematischen Formulierung**
$m$ ... Masse des Körpers
$(x(t),u(t))$ ... Position des Körpers zur Zeit $t$
$s(t)$ ... Zurückgelegter Weg (Bogenlänge)

2.Newton'sches Gesetz (in tangentialer Richtung, weil nur der Anteil in die Richtung beschleunigt, wo die Kugel überhaupt hinkann), d.h. Masse $\times$ Beschleunigung $=$ Kraft:
$$
m\frac{\mathrm{d}^2s}{\mathrm{d}t^2}=F\cdot e_t(x)=m\frac{g}{\sqrt{ 1+u'^2 }},
$$
$e_{t}(x)=\frac{1}{\sqrt{1+u'^2 }}\begin{pmatrix}1\\ u'\end{pmatrix}$ ... Einheitstangentialvektor an Kurve

**Gesucht:** $t(x)$ bzw. $x(t)$, $\frac{\mathrm{d}x}{\mathrm{d}t}=$ vertikale Geschwindigkeitskomponente.

Bogenlängenelement: $\sqrt{ 1+u'^2 }\mathrm{d}x=\mathrm{d}s\implies \sqrt{ 1+u'^2 }=\frac{\mathrm{d}s}{\mathrm{d}x}=\frac{\mathrm{d}s}{\mathrm{d}t}\frac{\mathrm{d}t}{\mathrm{d}x}$.
Einsetzen für $\sqrt{ 1+u'^2 }$ liefert:
$$
\implies g = \frac{\mathrm{d}^2s}{\mathrm{d}t^2} \sqrt{ 1+u'^2 }=\frac{\mathrm{d}^2s}{\mathrm{d}t^2}\frac{\mathrm{d}s}{\mathrm{d}t}\frac{\mathrm{d}t}{\mathrm{d}x}= \frac{1}{2}[\frac{\mathrm{d}}{\mathrm{d}t}(\frac{\mathrm{d}s}{\mathrm{d}t})^2]\frac{\mathrm{d}t}{\mathrm{d}x}
$$
"Durchdividieren" (bzw. Ableitung der Inversen- o.B.d.A. $x$ injektiv in $t$ also $b_{1}>$Minimum) liefert:
$$
\implies g \frac{dx}{dt}= \frac{1}{2}\frac{\mathrm{d}}{\mathrm{d}t} (\frac{\mathrm{d}s}{\mathrm{d}t})^2
$$
Links und rechts steht die totale Zeitableitung von etwas, d.h. integrieren nach der Zeit von $0$ bis $t$ liefert:
$$
gx=\frac{1}{2}(\frac{\mathrm{d}s}{\mathrm{d}t})^2 \text{ zum Zeitpunkt }t
$$
da $\frac{1}{2}\left( \frac{\mathrm{d}s}{\mathrm{d}t} \right)^2_{t=0}=0$, weil das innere genau die Tangentialgeschwindikeit ist und die Anfangsgeschwindigkeit ja generell $0$ ist. Bringt man die $2$ auf die andere Seite und zieht die Wurzel, erhält man wegen der Umrechnung des Bogenelements
$$
\sqrt{ 2gx}=\frac{\mathrm{d}s}{\mathrm{d}t}=\sqrt{ 1+u'^2 }\frac{\mathrm{d}x}{\mathrm{dt}}  
$$
"Kehrwert" bilden liefert 
$$
\frac{\mathrm{d}t}{\mathrm{d}x}=\sqrt{ \frac{1+u'^2}{2gx} } 
$$
Integriert man das von $0$ bis $b_{1}$ nach $x$, da man ja wissen will, wie viel Zeit vergangen ist, bis man $b_{1}$ erreicht hat, erhält man
$$
\text{Durchlaufzeit } = \frac{\int_{0}^{b_{1}}1}{\sqrt{ 2gx }}\sqrt{ 1+u'^2 }dx
$$
**Mathematische Problemstellung:**
Definiere die Funktionenmenge $U:=\{u \in C^1[0,b_{1}]|u(0)=0, u(b_{1})=b_{2} \}$ (erster Versuch einer Funktionenmenge, man kann das ggf. abschwächen und z.B. nur Integrierbarkeit der Ableitung fordern) und das Funktional
$$
\mathcal{F}:U\to \mathbb{R}, \mathcal{F} := \int_{0}^{b_{1}} \frac{1}{\sqrt{ 2gx }}\sqrt{ 1+u'^2 }dx
$$
Finde $u_{0}\in U$, so dass $\mathcal{F}(u_{0})$ minimal wird.

**Offene Fragen:**
- Ist $U$ eine/die geeignete Menge?
- Gibt es ein Minimum von $\mathcal{F}$ auf $U$? Wenn ja, ist es eindeutig?
- Wie findet man es?