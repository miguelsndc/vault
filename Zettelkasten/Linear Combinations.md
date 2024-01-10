---
tags: spaces, vector,
aliases: linear combination, linear combinations
---
A Linear combination of [[Vector|vectors]] in $n$-dimensional space is the sum of these vectors each weighted by some [[Real Numbers|real]] (or not) [[Scalar|scalar]] $\gamma$.
Given a set of $k$ vectors $v_{1}, v_{2}, \cdots, v_{k}$, and $\gamma_{i}\in \mathbb{R}, i=1, 2, \cdots, k$  their linear combinations is the vector $u$ resultant of the sum $\gamma_{1}v_{1}+\gamma_{2}v_{2}+\cdots+ \gamma_{k}v_{k}=u$. A Linear combination can be expressed in terms of [[Matrix Multiplication]], Suppose $v_{k}$ has $m$ components, then if we set each column of a matrix $A$ to be a vector $v_{k}$, $A$ will be a $m$ by $k$ matrix of column-vectors, by multiplying $A$ by the **vector of weights** $c$ $c= (\gamma_{1},\gamma_{2},\cdots,\gamma_{k})$, we obtain the same combination:
$$\begin{align*}
Ac &= \begin{pmatrix}
\cdot & \cdot & \cdot  & \cdot\\
\cdot & \cdot & \cdot  & \cdot\\
v_{1} & v_{2}  & \cdots & v_{k}\\
\cdot & \cdot & \cdot  & \cdot\\
\cdot & \cdot & \cdot  & \cdot\\
\end{pmatrix}
\begin{pmatrix}\gamma_{1}\\ \gamma_{2} \\ \vdots \\ \gamma_{k}\end{pmatrix}
&= \gamma_{1}v_{1}+ \gamma_{2}v_{2}+\cdots+\gamma_{k}v_{k}
\end{align*}$$
