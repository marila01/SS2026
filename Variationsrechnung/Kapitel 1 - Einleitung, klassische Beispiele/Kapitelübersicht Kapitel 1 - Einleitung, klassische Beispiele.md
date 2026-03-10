### Ziel der VO:
- Vorstellung von typischen Variationsproblemen und Anwendungen; 
- typische mathematische Fragestellungen (Existenz, Eindeutigkeit von Lösungen und deren qualitatives Verhalten); 
- typische (analytische) Lösungsstrategien.

Die Vorlesung gliedert sich in folgende Themenbereiche: 
1. Einleitung mit klassischen bzw. historischen Beispielen; [[Kapitelübersicht Kapitel 1 - Einleitung, klassische Beispiele]]. 
2. Klassische Theorie der Variationsrechnung (“indirekte Methode”). Hier ist das Ziel, notwendige und hinreichenge Bedingungen an Minimierer (des Variationsproblems) anzugeben; typischerweise sind diese ODEs oder PDEs. In einfachen Fällen (meist für nur ODEs) kann man deren eindeutige Lösbarkeit erkennen oder sie sogar explizit lösen (im Sinne von ‘ausrechnen’); [[Kapitelübersicht Kapitel 2 - Euler-Lagrange Gleichungen]], [[Kapitelübersicht Kapitel 3 - Zweite Variation, Konvexität]], [[Kapitelübersicht Kapitel 4 - Variationsprobleme mit Nebenbedingungen]]. 
3. Direkte Methode der Variationsrechnung. Hier ist das Ziel, mit funkionalanalytischen Methoden die Existenz und Eindeutigkeit von Minimierern von Variationsproblemen zu beweisen; [[Kapitel 5 - Existenztheorie für Minimierer]]. 
4. Weiterführende Probleme: In [[Kapitelübersicht Kapitel 6 - Nichtkonvexe Probleme]], [[Kapitelübersicht Kapitel 6 - Nichtkonvexe Probleme]] existiert meist kein Minimierer des betrachteten Variationsproblems. Daher werden Modifikationen des Ausgangsproblems bzw. des Lösungsbegriffs diskutiert, so dass die neuen Probleme (eindeutig) lösbar sind. In [[Kapitelübersicht Kapitel 8 - Parameterabhängige Variationsprobleme, Verzweigungstheorie]] hängen die Variationsprobleme von einem Parameter ab, und es wird die Parameterabhängigkeit der zugehörigen Lösungen betrachtet.

Viele Anwendungsprobleme sind generisch als Variationsprobleme formuliert. Auch für simple Beispiele ist deren Lösung aber oft schwierig (sowohl der Beweis der eindeutigen Lösbarkeit und erst recht das explizite Angeben der Lösung).

**Bsp. 1.1. Isoperimetrisches Problem**
![[Bsp.1.1 Isoperimetrisches Problem]]

**Bsp. 1.2. Minimalflächen
![[Bsp. 1.2. Minimalflächen]]

**Bsp. 1.3. Brachistochrone**
![[Bsp. 1.3. Brachistochrone]]

### Gegenstand der Vorlesung:
Untersuchung von Extremalstellen von Variationsintegralen (oder Energie-Funktionalen): 
$$u \mapsto F(u) := \int_{\Omega} F(x, u(x), \underbrace{\mathrm{D}u(x)}_{\text{Jacobi Matrix}} ) \mathrm{d}x : U → \mathbb{R} $$
auf Mengen $$U ⊂ \{u : Ω ⊂ \mathbb{R}^n → \mathbb{R}^N \}.$$
$F(x, z, p)$ heißt Lagrange Funktion, $z$ ist Platzhalter für den Vektor $u$, $p$ ist Platzhalter für die Matrix $Du$.

**Idee:** Verallgemeinerung von Extremwertmethoden für skalare Funktionen $f : U ⊂ \mathbb{R} → \mathbb{R}$:

- notwendige Bedingungen (analog zu $f' (x_{0}) = 0$ für $f \in C^1$ ) 
- hinreichende Bedingungen (analog zu $f''(x_{0}) \neq 0$ für $f ∈ C^2$ ). Typischerweise gibt es eine “Lücke” zwischen diesen beiden Bedingungen (vgl. $f(x)=x^3$, wo erste Bedingung gilt, zweite nicht und man genauer untersuchen muss, ob Extremum)
- Existenz globaler Extremwerte (analog zur Annahme der Extremwerte stetiger Funktionen auf Kompakta)

**Definition 1.4.**
![[Definition 1.4.]]
**Bsp. 1.5.**
![[Bsp. 1.5]]
**Bsp.1.6.**
![[Bsp.1.6.]]



