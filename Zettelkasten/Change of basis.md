---
tags: spaces
---
Let $\alpha$ and $\beta$ be both [[Theorems and Proofs for Basis and Dimension|basis]] of a [[Vector Space|space]] $V$, we can switch from $\alpha$ to $\beta$ via a [[Matrix Definition|matrix]] where each column is ***one vector of one basis written in terms of the other***, multiplying a vector will change it's coordinates with respect to the other basis.
___
Let $\alpha = \{u_{1},\cdots, u_{n}\}$  and $\beta = \{w_{1},\cdots, w_{n}\}$ be basis to $V$. Let $v \in V$. we can write $v$ as:
$$\begin{align*}
v&= x_{1}u_{1}+ \cdots+x_{n}u_{n}\\
v&= y_{1}w_{1}+\cdots+y_{n}w_{n}
\end{align*}$$
since we can relate the coordinates of $v$ with respect to $\alpha$ $[v]_{\alpha}=\begin{pmatrix}x_{1}\\ \vdots \\ x_{n} \end{pmatrix}$ with the coordinates of $v$ with respect to $\beta$: $[v]_{\beta}=\begin{pmatrix}y_{1}\\ \vdots \\ y_{n}\end{pmatrix}$, since $\alpha$ is a basis of $V$ we can write the vectors $w_{i}\in \beta$ as [[Linear Combinations|linear combinations]] of $u_{i}\in \alpha$, this means:
$$
\begin{cases}
w_{1} = a_{11}
\end{cases}
$$