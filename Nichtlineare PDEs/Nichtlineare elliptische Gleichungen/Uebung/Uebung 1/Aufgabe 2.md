Let $\Omega \subset \mathbb{R}^n$ be bounded and open, and $f:\Omega \times \mathbb{R}\to \mathbb{R}$ be a Carathéodory integrand. Let $M:\Omega \to \mathbb{R}$ be Lebesgue measurable. Prove that the map $x \mapsto f(x,M(x))$ is Lebesgue measurable on $\Omega$.
##### Proof:
Let $\Omega \subset \mathbb{R}^n$ be bounded, $A_{i}\subset \Omega, i=1,\dots,N$ measurable sets s.t. $\Omega=\bigcup_{i=1}^NA_{i}$, $a_{i}\in \mathbb{R}$.

Assume first, that $M=\sum_{i=1}^N \mathbb{1}_{A_{i}}a_{i}$.
For any $t \in \mathbb{R}$, it holds that
$$
\{ x \in \Omega\quad|\quad f(x,M(x))<t \}=\bigcup_{i=1}^N
\{ x \in A_{i}\quad|\quad f(x,a_{i})<t \}$$
is measurable, because it is the finite union of sets $\{ x \in A_{i} \quad|\quad f(x,a_{i})<t \}$, which are in turn measurable because $A_{i}$ and $f(.,a_{i})$ are measurable for fixed $a_{i}$.

We know that we can approximate Lebesgue-measurable functions with step-functions, meaning for every $M$ Lebesgue-measurable, there exists a sequence of stepfunctions $(M_{k})_{k}$, which converges to $M$ pointwise.

It follows, that $\forall  x \in \Omega: f(x,M_{k}(x))\to f(x,M(x))$ because $f$ is continous w.r.t. the second variable.
We conclude, that $x \mapsto f(x,M(x))$ is (as a pointwise limit of Lebesgue-measurable Functions) measurable.

![[Pasted image 20260317140110.png]]
![[Pasted image 20260317140521.png]]
