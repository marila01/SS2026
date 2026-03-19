Let $A \in \mathbb{K}^{n \times n}$ be regular,
let $D \in \mathbb{K}^{n \times n}$ be defined by

$$

D_{jk} := A_{jk}\delta_{jk},

$$

i.e., the diagonal of $A$.
Suppose that $D$ is regular, i.e., $D_{jj} \ne 0$ for all $j = 1,\dots,n$.
Then, the Jacobi iteration is the splitting scheme
$$

A = D + (A-D),

$$
i.e.,
$$

G := D,\qquad

H := -(A-D),\qquad

\Pi := G^{-1}H = -D^{-1}(A-D),\qquad

N := G^{-1} = D^{-1}.

$$

- Solve $Ds_k := b-Ax_k$
- Define $x_{k+1} := x_k + s_k$

Using upper indices $x^k := x_k$ for the iteration index and lower indices for the coefficients, this can explicitly be written as
$$

x_i^{k+1}

=

x_i^k

+

\frac{1}{A_{ii}}

\left(

b_i - \sum_{j=1}^n A_{ij}x_j^k

\right)

\qquad \text{for all } i=1,\dots,n.

$$