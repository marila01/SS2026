Ziel dieses Kapitels ist die Lösung von nichtlinearen elliptischen Differentialgleichungen vom Typ
$$
-\Delta u=f(x,u)\quad\text{ und}\quad -\mathrm{div}a(\nabla u)=f(x)
$$
Bei der ersten Gleichung handelt es sich um eine *semilineare* Gleichung (denn die höchste Ableitung ist linear in $u$), bei der zweiten Gleichung um eine *quasilineare Gleichung*, denn
$$
\mathrm{div}a(\nabla u)=\sum_{i=1}^n
\partial_{x_{i}}a_{i}(\partial x_{1},\dots,\partial_{x_{n}u})=\sum_{i,j=1}^n\frac{\partial a_{i}}{\partial z_{j}}(\nabla u)\partial_{x_{i}}\partial_{x_{j}}u .
$$
Um die Existenz bzw. Eindeutigkeit von Lösungen dieser Gleichungen zu beweisen, benutzen wir zwei grundlegende Prinzipien:
- Fixpunktsätze: Die Differentialgleichung wird als Fixpunktgleichung $S(u) = u$ umformuliert und die Existenz eines Fixpunktes $u$ wird bewiesen. Hierfür benötigen wir typischerweise Kompaktheitsresultate, die wir über sogenannte A-priori- Abschätzungen erhalten.
- A-priori-Abschätzungen: Dies sind Ungleichungen für $S(u)$, deren rechte Seite unabhangig von $u$ sind. Die Abschätzungen erhalten wir z.B. aus Maximumprinzipien oder aus der Monotonie der Nichtlinearitäten.

[[2.1 Semilineare Gleichungen]]
[[2.2 Monotone semilineare Gleichungen]]
[[2.3 Quasilineare Gleichungen]]
[[2.4 Drift-Diffusionsgleichungen]]

