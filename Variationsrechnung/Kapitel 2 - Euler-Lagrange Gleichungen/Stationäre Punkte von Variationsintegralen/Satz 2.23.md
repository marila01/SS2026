Zusätzlich zu den generellen Annahmen gelte $\frac{\partial F}{\partial p_{ij}}\in C^1(V)$.
Für eine Funktion $u\in C^2(\Omega;\mathbb{R}^N)\cap C^1(\bar{\Omega};\mathbb{R}^N)$ gelte
$$
\delta \mathcal{F}(u,\xi)=0 \quad \forall \xi \in C_{0}^\infty(\Omega; \mathbb{R}^N).
$$
Dann erfüllt $u$ die Euler-Lagrange Gleichung (EL-Gl.) von $\mathcal{F}$:
$$
\frac{\partial F}{\partial z_{i}}(x,u(x),Du(x))-\sum_{j=1}^n \frac{\partial}{\partial x_{j}}\left[  \frac{\partial F}{\partial p_{ij}}(x,u(x),Du(x))  \right] =0; \quad x \in \Omega; i=1,\dots,N 
$$

##### Beweis:
Sei $\psi \in C_{0}^\infty(\Omega,\mathbb{R}), \xi(x):=\psi(x)e_{i}$.
Aus $\delta \mathcal{F}(u,\xi)=0$ folgt:
$$
\int_{\Omega}\left( \frac{\partial F}{\partial z_{i}}\psi+\sum_{j=1}^n \frac{\partial F}{\partial p_{ij}}\frac{\partial \psi}{\partial x_{j}}    \right)dx=0
$$
Verwende
$$
\underbrace{\frac{\partial}{\partial x_{j}}\left(  \psi \frac{\partial F}{\partial p_{ij}}  \right) }_{\sum_{j} \text{ ist div}(\dots)}=\frac{\partial \psi}{\partial x_{j}}\frac{\partial F}{\partial p_{ij}} +\psi \frac{\partial}{\partial x_{j}}\frac{\partial F}{\partial p_{ij}} ,  
$$
Divergenzsatz und $\psi |_{\partial \Omega}=0$ liefert:
$$
\int_{\Omega}\left( \frac{\partial F}{\partial z_{i}} -\sum_{j=1}^n \frac{\partial}{\partial x_{j}}\frac{\partial F}{\partial p_{ij}}   \right)\psi dx=0 \quad \forall \psi \in C_{0}^\infty(\Omega)
$$
Die punktweise Gleichung folgt aus nachfolgendem Fundamentallemma der Variationsrechnung.

*Wichtig: Zuerst F nach p ableiten, dann (x,u,Du) einsetzen und nach x ableiten.*
