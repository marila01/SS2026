The Richardson iteration ([[Example (damped Richardson iteration)]]) is a splitting method
$$

A = I-(I-A)

$$
with $G:=I$, $H:=I-A$
and hence
$$

M = G^{-1}H = I-A,\qquad

N = G^{-1} = I,\qquad

\Phi(b,x) = (I-A)x + b.

$$
**Iteration:** $x_{k+1}=x_{k}-Ax_{k}+b=x_{k}-(Ax_{k}-b)$.
Bad for non-regular matrices $A$.
**Better (but not helpful for non-regular matrices):** Damped Richardson:  $G=\frac{1}{\lambda} I,H=\frac{1}{\lambda}I-A.$