---
tags: spaces, vector
---
A [[Vector Space]] or [[Linear Subspaces|subspace]] $V$ is *spanned* by a [[Sets|set]] of [[Vector|vectors]] $S = \{v_{1},v_{2},\cdots,v_{n}\}$, [[If and Only if|if and only if]] $\span(S) = V$, if so, then every vector in that space can be written as a [[Linear Combinations|linear combination]] of $S$. If those vectors are linearly [[Linear (In)dependence.|independent]] then this set is called a [[Basis and Dimension]], otherwise, just a *spanning set* of $V$.   
For example, two linearly [[Linear (In)dependence.|independent]] vectors span a [[Plane]] and three span a space.
There's infinetly many spanning sets for the same space, as well as infinitely many [[Basis and Dimension]].
Let $$
V= \Bigg\{(x,y,z,w) \in R^{4}\mid \begin{cases}
x+y+z=0 \\
2x-y-w=0 \\
\end{cases}
\Bigg\}
$$
Then we can find a spanning set for $V$ by finding the [[Row Reduced Echelon Form]] of the [[Augmented Matrix]] of $V$, then we can [[Parameterization of Rectangular System's Solutions|parameterize]] the solutions and find the [[Linear Combinations|linear combination]], those vectors are the *spanning set* of $V$ as well as a [[basis]] of $V$.
$$\begin{align*}
\begin{pmatrix}
1 & 1 & 1 & 0\\
2 & -1 & 0 & 0
\end{pmatrix}
\implies
\begin{pmatrix}
1 & 1 & 1 & 0\\
0 & -3 &-2 & 0
\end{pmatrix}
\implies
\begin{pmatrix}
1 & 0 & \frac{1}{2} & 0\\
0 & 1 & \frac{2}{3} & 0
\end{pmatrix}
\end{align*}$$so the parameterization is:
$$\begin{align*}
\begin{cases}
x&= \frac{-1}{3}z\\
y&= \frac{-2}{3}z\\
z&=z\\
w&=w\\
\end{cases},\;\;\;\; z,w\in\mathbb{R}
\end{align*}$$
And the vectors are $z(\frac{-1}{3}, \frac{2}{3},1,0)+w(0,0,0,1)$. We say that $\span\left(\left(\frac{-1}{3}, \frac{2}{3},1,0\right), (0,0,0,1)\right)= V$. 
