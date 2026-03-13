Es gelten die Voraussetzungen von [[Theorem 2.7 - Regularitaet linearer elliptischer Gleichungen]] und [[Theorem 2.5 - Existenz für semilineare Gleichungen]].
Dann existiert eine Lösung $u \in W^{2,q}(\Omega)$ von unserem nichtlinearen Problem.

##### Beweis:
Wir wissen, dass eine schwache Lösung $u^*$ von $L(u^*)=f(x,u^*)$ in $\Omega$ mit $u^*-g\in H_{0}^1(\Omega)$ existiert.
Halte $u^*$ fest. Wir setzen $\phi(x):=f(x,u^*(x))$.
Um [[Theorem 2.7 - Regularitaet linearer elliptischer Gleichungen]] auf das Problem
$$
\begin{cases}
L(u)=\phi(x) \text{ in } \Omega \\
u=g \text{ auf } \partial \Omega
\end{cases}
$$
anwenden zu können, müssen wir noch zeigen, dass
$$
|\phi(x)|=|f(x,u*(x))|\leq g(x)\in L^q(\Omega).
$$
Folglich ist $u^*$ eine Lösung den obenstehenden Problems.
Da lt. [[Theorem 2.7 - Regularitaet linearer elliptischer Gleichungen]] diese Lösung eindeutig ist, folgt, dass $u^* \in W^{2,q}(\Omega)$.
