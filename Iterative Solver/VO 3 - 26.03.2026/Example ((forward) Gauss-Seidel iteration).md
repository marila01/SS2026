Let $A \in \mathbb{K}^{n \times n}$ be regular.
Write
$$

A = L + D + U

$$
with
$$

L_{ik} =

\begin{cases}

A_{ik} & \text{for } i>k,\\

0 & \text{else},

\end{cases}

\qquad

U_{ik} =

\begin{cases}

A_{ik} & \text{for } i<k,\\

0 & \text{else},

\end{cases}

$$
Suppose that $D$ (and hence also $D+L$) is regular ($\iff A_{jj}\neq 0 \forall j$).
Then, the (forward) Gauss-Seidel iteration is the splitting scheme
$$

A = (D+L) + U,

$$
i.e.,
$$
G := D+L,\qquad
H := -U,\qquad
M := G^{-1}H = -(D+L)^{-1}U,\qquad
N := G^{-1} = (D+L)^{-1}.
$$
- Solve $(D+L)s_k = b-Ax_k \iff s_{k}=G^{-1}(b-Ax)$
- Define $x_{k+1} := x_k + s_k$

By forward substitution (because $L+D$ is lower-triangular), this can be written as:
$$
x_i^{k+1}
=
x_i^k
+
\frac{1}{A_{ii}}
\left(
b_i
-
\sum_{j=1}^{i-1} A_{ij}x_j^{k+1}
-
\sum_{j=i}^{n} A_{ij}x_j^k
\right)
\qquad \text{for all } i=1,\dots,n.
$$
Consequently, the only difference to the Jacobi method is that the newly computed coefficients $x_j^{k+1}$ immediately replace the old $x_j^k$ (no update-version).
Again, this $G$ has much more information about $A$.