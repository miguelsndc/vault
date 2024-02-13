---
tags: linear-transformations
---
In situations like:
"Find a [[Linear Transformations|linear transformation]] such that $T:\mathbb{R}^{3}\rightarrow \mathbb{R}^{3}$ with $\nu(T) = \{(x,y,z) \in \mathbb{R}^{3}\mid x+y-z=0  \}$ and $\im(T) = \{(x,y) \in \mathbb{R}^{3} \mid x=2y\}$"
We use a procedure similar to the proof of the [[Kernel-Image Theorem]].
- Start with a basis for the [[Kernel of a linear transformation|kernel]].
- Find a [[Theorems and Proofs for Basis and Dimension|basis]] of the [[Image of a linear transformation|image]].
- Complete with [[Linear (In)dependence.|linearly independent]] [[Vector|vectors]]
Find a [[Theorems and Proofs for Basis and Dimension|basis]] for the [[Kernel of a linear transformation|kernel]] with the usual procedure:
$$\begin{align*}
\nu(T) &= \begin{pmatrix}1 & 1 & -1\end{pmatrix}\implies\begin{cases}
x=z-y\\
y=y\\
z=z
\end{cases}\implies
\nu(T)= z(1,0,1)+y(-1,1,0)
\end{align*}$$
$\alpha = \{(1,0,1), (-1,1,0)\}$ is a basis for $\nu(T)$.
Same goes for $\im(T)$:
$$\begin{align*}
\im(T)&= \begin{pmatrix}1 & -2\end{pmatrix}\implies\begin{cases}
x=2y\\
y=y
\end{cases}\implies
\im(T) = y(2,1)
\end{align*}$$
$\{(2,1)\}$ is a basis for $\im(T)$.
Now completing with the independent vector is quite tricky, here we can use the vector [[Orthogonal Vectors|orthogonal]] to the [[Plane]] of $\nu(T)$, however, it's more optimal to pick a vector with the most number of zeroes as possible, in this case, it's $(0,0,1)$. Then we can write the [[Linear Transformations|transformation]] in terms of the [[Canonical Vectors]]. Now we have:
$$\begin{align*}
T(-1,1,0)&= (0,0)\\
T(1,0,1)&= (0,0)\\
T(0,0,1)&= (2,1)
\end{align*}$$
We can put the vectors suffering the transformation next to the basis in a matrix and find the [[Row Reduced Echelon Form]], since they're [[Linear (In)dependence.|linearly independent]], it'll always reach the [[Identity Matrix]], By doing so we find what the transformation is doing to the canonical vectors, and it's easier to reason and to calculate.
$$\begin{align*}
\begin{pmatrix}
-1 & 1 & 0  & \mid & 0 & 0 \\
1 & 0 & 1 & \mid & 0 & 0\\
0 & 0 & 1 & \mid & 2 & 1
\end{pmatrix}
\implies
\begin{pmatrix}
-1 & 1 & 0 & \mid & 0 & 0\\
0 & 1 & 1 & \mid & 0 & 0\\
0 & 0 & 1 & \mid & 2 & 1\\
\end{pmatrix}\\\\
\implies
\begin{pmatrix}
1 & -1 & 0 & \mid & 0 & 0\\
0 & 1 & 0 & \mid & -2 & -1\\
0 & 0 & 1 & \mid & 2 & 1\\
\end{pmatrix}
\implies
\begin{pmatrix}
1 & 0 & 0 & \mid & -2 & -1\\
0 & 1 & 0 & \mid & -2 & -1\\
0 & 0 & 1 & \mid & 2 & 1
\end{pmatrix}
\end{align*}$$
Thefore:
$$\begin{align*}
T(1,0,0)&= (-2,-1)\\
T(0,1,0)&= (-2,-1)\\
T(0,0,1)&= (2,1)\\
\end{align*}$$
Describing a general vector $(x,y,z)$ in terms of the canonical is trivial, that's why we convert it, see:
$$\begin{align*}
(x,y,z)&= x(1,0,0)+y(0,1,0)+z(0,0,1)\\
T(x,y,z)&= xT(1,0,0)+yT(0,1,0)+zT(0,0,1)
\end{align*}$$
Substituting:
$$\begin{align*}
T(x,y,z)&= x(-2,-1) + y(-2,-1)+z(2,1)\\
&= (-2x-2y+2z,-x-y+z)
\end{align*}$$
Therefore $T$ is defined by $T(x,y,z) = (-2x-2y+2z,-x-y+z)$. There are infinitely many such [[Linear Transformations]], since the [[Linear Transformations]] from one space to another is itself a [[Linear Subspaces|subspace]]. We can choose multiple of them by playing with different [[Theorems and Proofs for Basis and Dimension|basis]] for $\nu(T)$ and $\im(T)$ and also with the [[Linear (In)dependence.|linearly independent]] vectors at the end. But the initial condition is fulfilled and **the problem is solved**, finding the correct transformation depends on the situation.
