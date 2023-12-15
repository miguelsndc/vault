---
tags:
  - vector
aliases:
  - dot product
date: 2023-10-28
---
The **scalar product** of two [[Vector|vectors]] $\vec{u} = (x_{1}, y_{1})$ and $\vec{v}=(x_{2}, y_{2})$, is denoted by:
$$
\vec{u} \cdot \vec{v} = (x_{1}x_{2} + y_{1}y_{2}) = t
$$
Where $t$ is a constant called the **scalar product**.
# Properties:
These same properties apply for both $\mathbb{R}^{2}$ and $\mathbb{R^{3}}$.
- $\vec{u} \cdot \vec{u} \ge 0$ and $\vec{u} \cdot \vec{u} = 0 \iff \vec{u} = (0,0)$.
$$\begin{align*}
\vec{v}\cdot\vec{v} &= x_{1}^{2} + y_{1}^{2}
\end{align*}$$
- $\vec{u} \cdot \vec{v} = \vec{v} \cdot \vec{u}$ 
- $(k\cdot \vec{u})\vec{v} = k(\vec{v} \cdot \vec{u})$ 
- $\vec{U}(\vec{v}+\vec{w}) = \vec{U}\cdot v + \vec{U} \cdot w$

The dot product works the same for [[Vector Matrix Form]], but can be quickly defined as a [[Functions in Discrete Math|function]] like so:
$$\begin{align*}
dp(i)&= \sum_{j=0}^{n}a_{ij}x_{j}
\end{align*}$$
Where for each row $i$ of the **left most** matrix, we multiply each column with it's respective part in a [[Vector Matrix Form|column vector]], 