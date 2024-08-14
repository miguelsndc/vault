---
tags:
  - vector
aliases:
  - dot product
---
The **dot product** between two [[Vector|vectors]] $\vec{a}$ and $\vec{b}$ is the operation $\sum\limits a_{i}b_{i}$, where we multiply the respective components and add them together. Dot products have a wide variety of applications which comprises:
## Angle between two vectors
![[dot]]To find this angle between vectors $\vec{a}$ and $\vec{b}$ we can use the [[Law of Cosines]], that says that:
$$
\norm{c}^{2} = \norm{a}^{2}+\norm{b}^{2}-2\norm{a}\norm{b}\cos{\theta}
$$
So we solve this for $\theta$. But if we instead think of the dot product between $c$ and itself, and expand, we find:
$$\begin{align*}
c \cdot c &= (a-b)\cdot (a-b)\\
&= a\cdot a - 2(a\cdot b)+b\cdot b\\
\norm{c}^{2}&= \norm{a}^{2}+\norm{b}^{2}-2(a \cdot b)\\
\end{align*}$$
Since the angle between $c$ and $c$ is zero $\cos{0}= 1$, we see that this expression can be written equivalently using both dot product properties and the law of cosines, So a proof goes something like this, using the same drawing above.
$$
\begin{align*}
\norm{a }
\end{align*}
$$

