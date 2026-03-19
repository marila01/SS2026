Each strictly diagonal dominant matrix $A \in \mathbb{K}^{n \times n}$ is regular.

##### Proof:
Let $x \in \mathbb{K}^n$ with $Ax = 0$.
Then,
$$

(A-D)x = -Dx,

$$
i.e.,
$$

\sum_{\substack{k=1\\k\ne j}}^n A_{jk}x_k = A_{jj}x_j

\qquad \forall j=1,\dots,n.

$$
Choose index $j$ with $|x_j| = \|x\|_\infty$.
$$

\Rightarrow\quad

\|x\|_\infty

=

|x_j|

=

\left|

\frac{1}{A_{jj}}

\sum_{\substack{k=1\\k\ne j}}^n A_{jk}x_k

\right|

\le

\sum_{k\ne j}

\left|

\frac{A_{jk}}{A_{jj}}

\right|

|x_k|

<

\|x\|_\infty.

$$
and hence $x = 0$.
This proves $\ker(A)=\{0\}$ and hence $A \in \mathbb{K}^{n\times n}$ is regular.