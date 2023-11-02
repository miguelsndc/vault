---
tags:
  - avlc
  - vector
aliases:
  - normalization
date: 2023-11-02
---
If i want to find a [[Vector|vector]] $u$ that has same direction and orientation of a vector $v$, but [[Vector Norm|magnitude]] $1$ *(unitary)*. I need to multiply $v$ by a [[Scalar|scalar]] quantity that is the inverse of it's magnitude.
Recalling that [[Multiplication by Scalar|scalar multiplication]] by a positive value does not change direction and orientation, and since magnitudes can't be negative, i have a assurance that the scalar $k$ will be always positive, so my vector $u$ will never change direction, See:
$$\begin{align*}
u &= k \cdot v\\
||u||&= 1\\
||k\cdot v|| &= 1\\
|k| \cdot ||v|| &= 1 \;\; \text{Since k is secured to be positive i can drop the absolute value}\\
k \cdot ||v|| &= 1\\
k &= \frac{1}{||v||} 
\end{align*}$$
So the scalar we need is indeed the inverse of the original vector norm.