Minimalfläche: $\mathcal{F}(u)=\int_{\Omega}\sqrt{ 1+|\nabla u|^2 }dx$ für $N=1$.
Dann ist $\frac{\partial F}{\partial p_{j}}=\frac{p_{j}}{\sqrt{ 1+|p|^2 }}$.
Die natürlichen Randbedingungen sind dann 
$$
\frac{\nu \cdot \nabla u}{\sqrt{ 1+|u|^2 }}=0 \text{ auf }\partial \Omega
$$
**Geometrische Interpretation:**
![[Pasted image 20260310123812.png]]
Sei $\alpha$ der Winkel zwischen Graph($u$) und der Zylinderwand $\partial \Omega \times \mathbb{R}$:
$$
\mathrm{cos}(\alpha)=\begin{pmatrix}
\nu \\ 0
\end{pmatrix} \cdot n=\frac{-\nu \cdot \nabla u}{\sqrt{ 1+|\nabla u|^2 }}|_{\partial \Omega}=0
$$
d.h. glatte Minimalflächen ohne Randeinschränkungen schneiden $\partial \Omega \times \mathbb{R}$ orthogonal (z.B. Seifenhaut innerhalb eines Zylinders).