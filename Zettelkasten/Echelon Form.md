---
tags: systems, matrix
aliases: echelon, row echelon
---
Row Echelon form is a state a [[Matrix Definition|matrix]] encounters when gone through [[Elimination in Matrices|elimination]] it has this name for it's shape very similar to a stair or a echelon, and it followins certain properties:
- Non zero rows come first, do [[Row Exchanges]] if necessary, the [[Pivot|pivots]] are the **first entries** of these rows.
- Each pivot lies to the right of the pivot in the rows above, producing a echelon pattern
This shape is fundamental in linear algebra since it describes solutions for many problems and serves as a fundamental algebraic building block for the theory, it looks like:
$$\begin{align*}
\begin{pmatrix}
\alpha & * & * & * & * & * & * & * & * \\
0 & \alpha & * & * & * & * & * & * & * \\
0 & 0 & 0 & \alpha & * & * & * & * & * \\
0 & 0 & 0 & 0 & 0 & 0 & \alpha & * & * \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & \alpha \\
\end{pmatrix}
\end{align*}$$
Where the alpha characters represent the [[Pivot|pivots]] in this $5\times 9$ [[Matrix Definition|matrix]].