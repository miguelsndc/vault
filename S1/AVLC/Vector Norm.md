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
1. $||\vec{u}|| \ge 0$ 
$$\begin{align*}
||\vec{u}|| &= \sqrt{\vec{u} \cdot \vec{u}} \\\
\sqrt{\vec{u} \cdot \vec{u}} &= 0 \iff \vec{u}=(0,0) \therefore ||\vec{u}|| \ge 0
\end{align*}$$
2. $||K \cdot \vec{v}||$ = $|K| \cdot ||\vec{v}||$
$$\begin{align*}
||K\cdot \vec{v}||&= \sqrt{(K\cdot\vec{u})(K\cdot\vec{u})}\\
&= \sqrt{K^{2}}\cdot\sqrt{\vec{u} \cdot \vec{u}}\\
&= |K| \cdot ||\vec{u}||
\end{align*}$$
1. *Cauchy-Schwarz Inequality*: $|\vec{u} \cdot \vec{v}| \le ||\vec{u}|| \cdot ||\vec{v}||$
Let the vectors $\vec{u}$ and $\vec{v}$ and $\overrightarrow{u -v}$ form a non-right triangle in a two-dimensional plane, with $\theta$ as the angle that $\vec{u}$ and $\vec{v}$ form together, Let the sides **be their norms**. By the law of cosines we have, Here well ignore the upper arrow notation for readability purposes.
$$
\begin{align*}
&||u-v||^{2} =  ||u||^{2}+||v||^{2}-2||u||\cdot||v||\cos{\theta}\\
&\text{Simplify } ||u-v||^{2}\\
&||u-v||^{2}= u(u-v) + (u-v)(-v)\\
&= u\cdot u - vu -vu+v \cdot v\\
&= ||u||^{2}-2vu+||v||^{2}\\
&\text{Now we have:}\\
&||u||^{2}-2u\cdot{v}+||v||^{2}= ||u||^{2}+||v||^{2}-2||u||\cdot ||v||\cos(\theta)\\
&u\cdot v= ||u||\cdot||v||\cos(\theta)\\
&\cos{\theta}= \frac{u\cdot{v}}{||u||\cdot{||v||}}\\
&\text{We know that:}\\
&-1 \le \cos{\theta} \le 1\\
&|\cos{\theta}| \le 1\\
&\text{So:}\\
&\mid \frac{u\cdot{v}}{||u||\cdot{||v||}}\mid \le 1\\
&\frac{1}{||u||\cdot{||v||}} \cdot |u\cdot{v}| \le 1\\
&|u\cdot{v}| \le ||u|| \cdot ||v||
\end{align*}
$$
From here we take a few identities, like:
$$\begin{align*}
&\cos{\theta}= \frac{u\cdot{v}}{||u||\cdot{||v||}}\\
\end{align*}$$

