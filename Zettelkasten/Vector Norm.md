---
tags: vector
aliases: magnitude
---
The *norm* of a [[Vector]] denotes the **length** of that vector according to some [[Inner Product|inner product]] $\innp{,}$. Let $V$ be a [[Vector|vector]] space with inner product $\innp{,}$. Then the norm of $V$ with respect to this $i.p$ is given by:
$$\begin{align*}
\norm{v}&= \sqrt{\innp{v,v}}
\end{align*}$$
If $\norm{v} = 1$, then $v$ is **normalized**, and is called a [[Vector Normalization|unitary vector]], Every non-zero vector can be normalized by doing $u = \frac{v}{\norm{v}}$.
Some **properties** are:
- $\norm{v} \ge 0$ and $\norm{v} = 0 \iff v = \vec{0}$ .
From the properties of inner product we have: $\norm{v} \ge 0$ because $\sqrt{\innp{v,v}}= 0 \implies \innp{v,v}= 0 \implies v = \vec{0}$. and obviously $\innp{v,v} \ge 0$ if $v \ne \vec{0}$
- $\norm{\alpha v} = \abs{\alpha} \cdot \norm{v}$ for $\alpha \in \R$.
  $\norm{\alpha v}= \sqrt{\innp{\alpha v, \alpha v}}= \sqrt{\alpha^{2} \innp{v,v}}= \abs{\alpha} \cdot \innp{v,v}$.  
- $\abs{\innp{v,w}} \le \norm{v} \cdot \norm{w}$ is the [[Schwarz Inequality]].
- $\norm{v + w} \le \norm{v} + \norm{w}$; proof is by faith in me.

## Where this comes from
This notion comes from the euclidean $2$D or $3$D space, where the length of a vector can be found through the [[Pythagorean Theorem]]. Let $v = (x,y)$ be rooted at the origin.
the $y$ component of $v$ is the height of a [[Right Triangle]]. 
the $x$ component of $v$ is the base of the right triangle.
Therefore the hypothenuse, or the length of the vector, is given by: $\sqrt{x^{2}+y^{2}}$. This also works for $3$D space, the length will be $\sqrt{x^{2} + y^{2} + z^{2}}$, but notice that if we are equipped with a regular [[Dot Product|dot product]], this is just the square root of the dot product of $v$ with itself, generalizing for $n$-dimensional space and for a arbitrary [[Inner Product|inner product]], this will be $\sqrt{\innp{v,v}}$.