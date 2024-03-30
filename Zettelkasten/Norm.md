---
tags: vector
---
The *norm* of a [[Vector]] denotes the **length** of that vector according to some [[Inner Product|inner product]] $\innp{,}$. Let $V$ be a [[Vector|vector]] space with inner product $\innp{,}$. Then the norm of $V$ with respect to this $i.p$ is given by:
$$\begin{align*}
\norm{v}&= \sqrt{\innp{v,v}}
\end{align*}$$
If $\norm{v} = 1$, then $v$ is **normalized**, and is called a [[Vector Normalization|unitary vector]], Every non-zero vector can be normalized by doing $u = \frac{v}{\norm{v}}$.
Some **properties** are:
- 






## Where this comes from
This notion comes from the euclidean $2$D or $3$D space, where the length of a vector can be found through the [[Pythagorean Theorem]]. Let $v = (x,y)$ be rooted at the origin.
the $y$ component of $v$ is the height of a [[Right Triangle]]. 
the $x$ component of $v$ is the base of the right triangle.
Therefore the hypothenuse, or the length of the vector, is given by: $\sqrt{x^{2}+y^{2}}$. This also works for $3$D space, the length will be $\sqrt{x^{2} + y^{2} + z^{2}}$, but notice that if we are equipped with a regular [[Scalar Product|dot product]], this is just the square root of the dot product of $v$ with itself, generalizing for $n$-dimensional space and for a arbitrary [[Inner Product|inner product]], this will be $\sqrt{\innp{v,v}}$.