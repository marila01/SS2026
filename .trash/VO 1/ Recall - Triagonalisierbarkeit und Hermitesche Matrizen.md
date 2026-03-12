# Recall - Triagonalisierbarkeit und Hermitesche Matrizen

Jede Matrix $A\in\mathbb{K}^{n\times n}$ ist über $\mathbb{C}$ triangulierbar.

Das heißt, es gibt eine reguläre Matrix $T\in\mathbb{C}^{n\times n}$ und eine obere Dreiecksmatrix $U\in\mathbb{C}^{n\times n}$ mit

$$
U = T^{-1}AT.
$$

Die Diagonalelemente von $U$ sind die Eigenwerte von $A$.

Ist $A=A^H$ hermitesch, dann ist $A$ diagonalisierbar.

Dann gibt es eine unitäre Matrix $Q$ und eine Diagonalmatrix $D$ mit

$$
D = Q^H A Q,
\qquad Q^H Q = I.
$$

Die Diagonaleinträge von $D$ sind reell und genau die Eigenwerte von $A$.

Die Spalten von $Q$ sind orthonormale Eigenvektoren von $A$.