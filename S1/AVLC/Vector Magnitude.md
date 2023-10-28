---
tags:
  - avlc
  - vector
aliases:
  - magnitude
date: 2023-10-26
---
The **magnitude, length or norm** $a$ of a [[Vector]] $\vec{v}$ plotted within a two-dimensional system is:
$$\begin{align*}
\vec{v} &= (x_{1},y_{1})\\
||\vec{v}||^{2} &= x_{1}^{2} + y_{1}^{2}\\
||\vec{v}|| &= \sqrt{x_{1}^{2} + y_{1}^{2}\\}
\end{align*}$$

The $||\vec{v}||$ syntax stands for **norm**, note that the result of this pythagorean theorem is exactly the [[Scalar Product]] of $\vec{v}$ with itself, so we can say that:

> The norm of a vector $\vec{v}$ is the square root of the scalar product of $\vec{v}$ with itself.

Or

> The norm of a vector $\vec{v}$ is the distance from the origin to the endpoint of $\vec{v}$. 
> $dist(O, v) = ||\vec{v}||$

Since the distance from the origin and self scalar product leads to the same return value.

With $\mathbb{R}^{3}$ it's:
$$\begin{align*}
||\vec{v}|| &= \sqrt{x_{1}^{2}+ y_{1}^{2}+ z_{1}^{2}}
\end{align*}$$
#### Properties
- $||\vec{u}|| \ge 0$ 
$$\begin{align*}
||\vec{u}|| &= \sqrt{\vec{u} \cdot \vec{u}} \\\
\sqrt{\vec{u} \cdot \vec{u}} &= 0 \iff \vec{u}=(0,0) \therefore ||\vec{u}|| \ge 0
\end{align*}$$
- $||K \cdot \vec{v}||$ = $|K| \cdot \vec{v}$