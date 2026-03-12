# Lemma - Fehlerabschätzung mit Konditionszahl

Sei $A\in\mathbb{K}^{n\times n}$ regulär.

Seien $x,\tilde{x},b,\tilde{b}\in\mathbb{K}^n$ mit $b\ne 0$ und

$$
Ax=b,\qquad A\tilde{x}=\tilde{b}.
$$

Dann gilt

$$
\frac{||x-\tilde{x}||}{||x||}
\le
\operatorname{cond}_{||\cdot||}(A)\,
\frac{||b-\tilde{b}||}{||b||}.
$$

Die Abschätzung ist scharf.