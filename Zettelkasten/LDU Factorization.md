---
tags: systems
---
One Thing about [[A = LU Factorization]], is that $LU$ is *unsymmetric*, this can be easily fixed by factoring $U$ into two [[Matrix Definition|matrices]], one diagonal [[Pivot|pivot]] matrices, and another matrix where every row has been divided by it's respective pivot, See:
$$\begin{align*}
U=\begin{pmatrix}
d_{1}& & &\\
& d_{2} & &\\
& & \ddots\\
& & & d_{n}
\end{pmatrix}=
\begin{pmatrix}
1 & \frac{u_{12}}{d_{1}}& \frac{u_{13}}{d_{1}}\end{pmatrix}
\end{align*}$$
