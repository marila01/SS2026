## Aufgabe 57

Bestimmen Sie alle Häufungspunkte sowie
$$
\limsup_{n\to\infty} a_n
\quad\text{und}\quad
\liminf_{n\to\infty} a_n
$$
der Folge
$$
a_n = (-1)^n \cdot n^{\,(-1)^{\frac{n(n+1)}2}+1} + \cos\left(\frac{n\pi}{2}\right).
$$

## Lösung

Wir untersuchen die Folge nach den Restklassen von $n$ modulo $4$.

### 1. Der Exponent

Zunächst betrachten wir
$$
(-1)^{\frac{n(n+1)}2}.
$$
Die Parität von $\frac{n(n+1)}2$ hängt von $n \bmod 4$ ab:

- Für $n \equiv 0 \pmod 4$ ist $\frac{n(n+1)}2$ gerade.
- Für $n \equiv 1 \pmod 4$ ist $\frac{n(n+1)}2$ ungerade.
- Für $n \equiv 2 \pmod 4$ ist $\frac{n(n+1)}2$ ungerade.
- Für $n \equiv 3 \pmod 4$ ist $\frac{n(n+1)}2$ gerade.

Also gilt
$$
(-1)^{\frac{n(n+1)}2}
=
\begin{cases}
1, & n \equiv 0,3 \pmod 4,\\
-1, & n \equiv 1,2 \pmod 4.
\end{cases}
$$

Damit wird der Exponent
$$
(-1)^{\frac{n(n+1)}2}+1
=
\begin{cases}
2, & n \equiv 0,3 \pmod 4,\\
0, & n \equiv 1,2 \pmod 4.
\end{cases}
$$

### 2. Der Cosinus-Term

Außerdem ist
$$
\cos\left(\frac{n\pi}{2}\right)
=
\begin{cases}
1, & n \equiv 0 \pmod 4,\\
0, & n \equiv 1 \pmod 4,\\
-1, & n \equiv 2 \pmod 4,\\
0, & n \equiv 3 \pmod 4.
\end{cases}
$$

### 3. Fallunterscheidung nach $n \bmod 4$

#### Fall $n=4k$

Dann ist
$$
a_{4k}
=
(-1)^{4k}(4k)^2 + \cos(2k\pi)
=
(4k)^2+1.
$$
Also gilt
$$
a_{4k}\to +\infty.
$$

#### Fall $n=4k+1$

Dann ist der Exponent gleich $0$, also $n^0=1$. Daher
$$
a_{4k+1}
=
(-1)^{4k+1}\cdot 1 + \cos\left(\frac{(4k+1)\pi}{2}\right)
=
-1+0
=
-1.
$$

#### Fall $n=4k+2$

Wieder ist der Exponent gleich $0$, also
$$
a_{4k+2}
=
(-1)^{4k+2}\cdot 1 + \cos\left(\frac{(4k+2)\pi}{2}\right)
=
1+(-1)
=
0.
$$

#### Fall $n=4k+3$

Dann ist der Exponent gleich $2$, also
$$
a_{4k+3}
=
(-1)^{4k+3}(4k+3)^2 + \cos\left(\frac{(4k+3)\pi}{2}\right)
=
-(4k+3)^2+0.
$$
Also gilt
$$
a_{4k+3}\to -\infty.
$$

### 4. Häufungspunkte

Die Teilfolge $$(a_{4k+1})$$ ist konstant gleich $-1$, also ist $-1$ ein Häufungspunkt.

Die Teilfolge $$(a_{4k+2})$$ ist konstant gleich $0$, also ist $0$ ein Häufungspunkt.

Die Teilfolge $$(a_{4k})$$ geht gegen $+\infty$, und $$(a_{4k+3})$$ geht gegen $-\infty$. Diese liefern keine endlichen Häufungspunkte in $\mathbb{R}$.

Also sind die Häufungspunkte in $\mathbb{R}$
$$
\boxed{\{-1,\,0\}}.
$$

### 5. Limes superior und limes inferior

Da eine Teilfolge gegen $+\infty$ geht, gilt
$$
\boxed{\limsup_{n\to\infty} a_n = +\infty.}
$$

Da eine Teilfolge gegen $-\infty$ geht, gilt
$$
\boxed{\liminf_{n\to\infty} a_n = -\infty.}
$$

## Ergebnis

$$
\boxed{\text{Häufungspunkte in } \mathbb{R}: -1,\ 0}
$$

$$
\boxed{\limsup_{n\to\infty} a_n = +\infty}
$$

$$
\boxed{\liminf_{n\to\infty} a_n = -\infty}
$$