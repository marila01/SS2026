With the same notation as in [[Theorem 2.3 - Fixpunktsatz von Schauder]], show that for every $j \in \mathbb{N}$ we can construct a map $F_{j}:K \to K_{j}$ such that
1. $||F_{j}(x)-x||\leq \frac{1}{j}$ for every $x \in K$.
2. $F_{j}\circ S|_{K_{j}}:K_{j}\to K_{j}$ is continuous.

##### Solution:
Let $x \in K$, $i=1,\dots,N_{j}$.
Let $\tilde{\lambda_{i}}(x):=d\left( x,K\setminus B_{\frac{1}{j}}(x_{i}) \right)\geq 0$.
We know from ANA 1 UE 11 Aufgabe 6, that for $x \in K$:
$d\left( x,K\setminus B_{\frac{1}{j}}(x_{i}) \right)=0 \iff x \in K \setminus B_{\frac{1}{j}}(x_{i})$, because $K \setminus B_{\frac{1}{j}}(x_{i})$ is closed and nonempty and $\{ x \}$ is compact and nonempty. 

We also know from ANA 1 UE 11 Aufgabe 6, that the mapping $x \mapsto d(x,A)$ is continous.
Let $\lambda(x):=\sum_{i=1}^{N_{j}}\tilde{\lambda}_{i}(x)>0$, because $K \subset\bigcup_{i=1}^{N_{j}}B_{\frac{1}{j}}(x_{i})$.

Let $\lambda_{i}(x):=\frac{\tilde{\lambda}_{i}(x)}{\lambda(x)}\geq 0$, continous because $\tilde{\lambda_{i}}(x),\lambda(x)$ are continous.

Let $F_{j}(x):=\sum_{i=1}^{N_{j}}\lambda_{i}(x)x_{i}$. Then $F_{j}$ is continous.
$F_{j}:K\to K_{j}$, because $\sum_{i=1}^{N_{j}}\lambda_{i}=\frac{1}{\lambda}\sum_{i=1}^{N_{j}}\tilde{\lambda}_{i}(x)=1$.

We now show that $\forall x \in K$: $||F_{j}(x)-x||< \frac{1}{j}$.
Let $x \in K$. 
$$
\begin{align}
||F_{j}(x)-x||&=||\sum_{i=1}^{N_{j}}\lambda_{i}(x)x_{i}-x|| \\
&=||\frac{1}{\lambda(x)}\sum_{i=1}^{N_{j}}\tilde{\lambda}_{i}(x)x_{i}-x|| \\

&=\frac{1}{\lambda(x)} ||\sum_{i=1, \lambda_{i}(x)\neq 0}^{N_{j}}\tilde{\lambda}_{i}(x)(x_{i}-x)|| \\
&\leq \frac{1}{\lambda(x)}\sum_{i=1, \lambda_{i}(x)\neq 0}^{N_{j}}\tilde{\lambda}_{i}(x)\underbrace{||x_{i}-x||}_{<\frac{1}{j}} \\
&\leq \frac{\lambda(x)}{\lambda(x)} \frac{1}{j}=\frac{1}{j}
\end{align}
$$
 Also, $S|_{K_{j}}$ is continous and $F_{j}$ is continous, so $F_{j}\circ S|_{K_{j}}$ is continous.
 
![[Pasted image 20260316200838.png]]![[Pasted image 20260316200851.png]]
