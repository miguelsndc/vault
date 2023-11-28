---
tags:
  - vector
aliases: 
date: 2023-11-14
---
We can determine a [[Vector|vector]] that is simultaneously perpendicular to two other vectors. We can do so by putting the two vectors in a determinant with the [[Canonical Vectors]] and working through it. 

Curiously the [[Vector Norm|magnitude]] of the cross product is exactly equal to the area of the [[vault/content/basics/Parallelogram|Parallelogram]]formed by the other two vectors, hence this operation is extremely useful to calculate areas, but finding perpendicular vectors is a equally important operation. 

The operation is denoted by $u \times v$.
___
#### Properties

- Cross Product **is not** commutative. From the inner working of matrices we see that modifying one column or line in it changes the sign, Therefore:
$$\begin{align*}
u\times v \ne v \times u
\end{align*}$$
But if we change **two lines or two columns** we keep the same result, so:
$$\begin{align*}
u \times v&= -v\times u
\end{align*}$$
But note that both $u\times v$ and $v \times u$ are perpendicular to $u$ and $v$. They just fall in opposite directions.
- Cross Product is distributive:
$$\begin{align*}
(u+v)\times w&= u\times w+v\times w\\
w\times(u+v)&= w\times u + w\times v
\end{align*}$$
- Scalar Multiplication
$$\begin{align*}
(ku)\times v=u\times(kv)=k(u\times v)
\end{align*}$$
For whatever vectors $u$ and $v$ or number $k$.
- **NOT ASSOCIATIVE**:
$$\begin{align*}
u\times(v\times w)\ne (u\times v)\times w
\end{align*}$$
- $||u\times v||=||u||\cdot ||v|| \sin{\theta}$. Proof: 
$$\begin{align*}
||u\times v||^{2}=||u||^{2}\cdot||v||^{2}-(u\cdot v)^{2}
\end{align*}$$
Take this for granted, too much work to prove it, but we'll use it:
$$\begin{align*}
||u\times v||^{2}&= ||u||^{2}\cdot||v||^{2}-(u\cdot v)^{2}\\
&= ||u||^{2}\cdot ||v||^{2}-||u||^2\cdot||v||^{2}\cos^2{\theta}\\
&= ||u||^{2}\cdot ||v||^{2}(1-\cos^2{\theta})\\
&= ||u||^{2}\cdot||v||^{2}\sin^{2}{\theta}\\\\
&||u\times v||=||u||\cdot||v||\sin{\theta}
\end{align*}$$
So the area of a paralellogram is also denoted by $||u||\cdot ||v||\sin{\theta}$.