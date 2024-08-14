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
Since the angle between $c$ and $c$ is zero $\cos{0}= 1$, we see that this expression can be written equivalently using both dot product properties and the law of cosines, So a proof goes something like this, using the same drawing above:

- Take the length of the vector $c = a - b$ using dot product:
$$
\begin{align*}
\norm{a - b}^{2}&= (a-b)\cdot(a-b)\\
&= \norm{a}^{2} - 2a \cdot b+\norm{b}^{2}
\end{align*}
$$
- And with law of cosines:
$$\begin{align*}
\norm{a-b}^{2}&= \norm{a}^{2}+\norm{b}^{2}-2\norm{a}\norm{b}\cos{\theta}
\end{align*}$$
By definition both ways should result in the same value, so equating both we obtain:
$$\begin{align*}
\norm{a}^{2} - 2a \cdot b+\norm{b}^{2} &=\norm{a}^{2}+\norm{b}^{2}-2\norm{a}\norm{b}\cos{\theta}\\
-2a\cdot b&= -2\norm{a}\norm{b}\cos{\theta}\\
a \cdot b &= \norm{a}\norm{b}\cos{\theta}
\end{align*}$$
So we can easily find the angle between $a$ and $b$ by just letting $\theta= \cos^{-1}(\frac{a\cdot b}{\norm{a}\norm{b}})$.
From this we get a ton of useful tricks:
- Test orthogonality between vectors, $i.e$ $a \cdot b = 0$ since $\cos{\frac{\pi}{2}}= 0$.
- The **sign** of the dot product depends directly on the sign of the cosine, since lengths are always positive, this implies:
	- $a \cdot b > 0 \implies 0 <= \theta< 90^{\circ} = \frac{\pi}{2}$   
	- $a \cdot b = 0 \implies \theta = 90^{\circ}=\frac{\pi}{2}$ 
	- $a \cdot b < 0 \implies \theta > \frac{\pi}{2}=90^{\circ}$.
	If two vectors point somewhat in the same direction their dot product is $\gt 0$. If they're orthogonal, $0$, if pointing in different directions, $\lt 0$.
We can even de