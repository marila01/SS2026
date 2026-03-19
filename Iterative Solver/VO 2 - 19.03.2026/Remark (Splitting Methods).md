For a splitting method $A=G-H$, it holds
$$

Ax^\ast = b

\Longleftrightarrow

Gx^\ast - Hx^\ast = b

\Longleftrightarrow

x^\ast = G^{-1}Hx^\ast + G^{-1}b.

$$
Hence, splitting methods are consistent.
The fixed point iteration reads
$$

x_{k+1}

= G^{-1}Hx_k + G^{-1}b

= (I-G^{-1}A)x_k + G^{-1}b

= x_k + G^{-1}(b-Ax_k)

$$
Richardson-type formulation,
where $G \ne A$, but is easier to solve.

Note that $G^{-1}$ will **never** be computed. Instead,
- solve $Gs_k := b-Ax_k$,
- define $x_{k+1} := x_k + s_k$.