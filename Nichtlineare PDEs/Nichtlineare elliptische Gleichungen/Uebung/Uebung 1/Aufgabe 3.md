Let$B_{1}, B_{2}$ be two Banach space and let $T:B_{1}\to B_{2}$ be a linear, continous operator.
Prove that if $v_{n} \rightharpoonup v$ weakly in $B_{1}$, then $T(v_{n})\rightharpoonup T(v)$ weakly in $B_{2}$.

##### Proof:
$v_{n}\rightharpoonup v$ weakly in $B_{1} \iff \forall F \in B_{1}':\langle F,v_{n}\rangle_{B_{1}'}\to\langle F,v\rangle_{B_{1}'}$.

Let $\tilde{F}\in B_{2}'$, then $\tilde{F}\circ T \in B_{1}'$, because the composition of two linear, continous operators is also linear and continous,
$\langle \tilde{F},T(v_{n})\rangle_{B_{2}'}=\langle \tilde{F}\circ T,v_{n}\rangle_{B_{1}'}\to \langle \tilde{F}\circ T,v\rangle_{B_{1}'}=\langle \tilde{F}, T(v)\rangle_{B_{2}'}$.
