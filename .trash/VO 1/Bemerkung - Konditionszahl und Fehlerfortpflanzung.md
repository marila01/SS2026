# Bemerkung - Konditionszahl und Fehlerfortpflanzung

Die Konditionszahl ist der Worst-Case-Faktor für die Fehlerfortpflanzung.

Sie beschreibt, wie stark sich eine Störung der rechten Seite $b$ auf die Lösung $x$ auswirken kann.

Bei direkten Lösern wie der Gauß-Elimination kann zusätzliche Fehlerfortpflanzung auftreten, etwa durch Faktorisierungen wie $A=LU$.

Im ungünstigen Fall können dabei Faktoren wie $\operatorname{cond}(L)\operatorname{cond}(U)$ größer sein als $\operatorname{cond}(A)$.