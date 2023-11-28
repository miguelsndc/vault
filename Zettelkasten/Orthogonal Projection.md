---
tags:
  - vector
  - geometry/analytic
aliases:
  - orthogonal projection
  - projection
date: 2023-11-02
---
Recalling the orthogonality concepts in [[Orthogonality Between Vectors]], we say that two [[Vector|vectors]] are orthogonal between each other if their [[Scalar Product]] is $0$, the direct consequence of a $0$ scalar product is a $90\degree$ angle between the vectors.

If i have two non-orthogonal vectors $u$ and $v$, and want to *orthogonally project* $u$ over $v$, this means, finding a vector $w$ that's multiple of $v$ *(has same direction and orientation)*, such as when we do $u - w$ we get a new vector that is orthogonal to $v$. See:

![[Orthogonal_Projection.excalidraw]]
We can clearly see that $w$ is a multiple of $v$, meaning $w = k \cdot v$
And if $u - w$ is orthogonal to $v$, we can say that $(u-v)\cdot v = 0$, See:
$$\begin{align*}
w&= k\cdot v\\
(u-w)\cdot v &= 0\\
(u-k\cdot v)&= 0\\
u\cdot v-k\cdot v\cdot v&= 0\\
u\cdot v&= k\cdot v\cdot v \\
k&= \frac{u\cdot v}{v \cdot v}\\
\text{Recalling } w &= k\cdot v\\
w &= \frac{u\cdot v}{v \cdot v} \cdot v
\end{align*}$$
From this we find the vector $w$ that is right below $u$. to find the vector that is orthogonal to $v$, just do $u - w$ where $w = proj(u/v)$. 