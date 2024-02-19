---
tags: linear-transformations
---
Consider $T:V \rightarrow W$ [[Linear Transformations|linear transformation]] and two [[Theorems and Proofs for Basis and Dimension|basis]] $\alpha=\{v_{1},\cdots, v_{n}\}, \beta = \{w_{1},\cdots, w_{n}\}$ where $\dim{V} = n$ and $\dim{W} = m$,
Let $v \in V$, so $v$ can be written as $v= a_{1}v_{1} + \cdots + a_{n}v_{n}$, after applying $T$, we obtain $Tv = a_{1}Tv_{1}+ \cdots + a_{n}Tv_{n}$. 
We want to find $[w]_{\beta} = [Tv]_{\beta}$.
- Note that if $\{Tv_{1}, \cdots, Tv_{n}\}$ was a [[Theorems and Proofs for Basis and Dimension|basis]], $\gamma$, then $[Tv]_{\gamma} = \begin{pmatrix}a_{1}\\ \vdots \\ a_{n}\end{pmatrix}$, the actual coefficients of $v$. Since transformations preserve the [[Coordinates]]. However, this happens [[If and Only if|if and only if]] $T$ is a [[Isomorphism]], if it's not, then the [[Image of a linear transformation|image]] isn't a [[Theorems and Proofs for Basis and Dimension|basis]] therefore the coordinates aren't exactly the same.

Write each $Tv_{i}$ as a [[Linear Combinations|linear combination]] of $\beta$, and collecting terms:
$$\begin{align*}
\begin{cases}
Tv_{1}=c_{11}w_{1}+ \cdots +c_{m1}w_{1}\\
\vdots\\
Tv_{n}=c_{1n}+ \cdots + c_{mn}w_{m}
\end{cases}
\end{align*}$$
Note that:
$$\begin{align*}
[Tv_{1}]_{\beta}=\begin{pmatrix}c_{11}\\ \vdots \\ c_{m1} \end{pmatrix}\;\;
[Tv_{n}]_{\beta}=\begin{pmatrix}c_{1n}\\ \vdots \\ c_{mn} \end{pmatrix}\\
\end{align*}$$
So, going back to find $[Tv]_{\beta}$:
$$
\begin{align*}
w = Tv &= a_{1}Tv_{1} + \cdots + a_{n}Tv_{n}\\
&= 
a_{1}(c_{11}w_{1}+\cdots+c_{m1}w_{m})+\\
\vdots\\+
&a_{n}(c_{1n}w_{1}+\cdots +c_{mn}w_{m})
\end{align*}$$
Now write $Tv$ in function of $\beta$:
$$\begin{align*}
Tv&= (a_{1}c_{11}+\cdots+a_{n}c_{1n})w_{1}+\cdots+(a_{1}c_{m1}+\cdots+a_{n}c_{mn})w_{m}
\end{align*}$$
So:
$$\begin{align*}
[w]_{\beta}&= [Tv]_{\beta}=
\begin{pmatrix}
a_{1}c_{11}+ \cdots + a_{n}c_{1n}\\
\vdots\\
a_{1}c_{m1} + \cdots a_{n}c_{mn}
\end{pmatrix}
\end{align*}$$
$[Tv]_{\beta}$ can be written as a product of two [[Matrix Definition|matrices]], as follows:
$$\begin{align*}
[Tv]_{\beta}=
\begin{pmatrix}
c_{11} & \cdots & c_{1n}\\
\vdots\\
c_{m1} & \cdots & c_{mn}
\end{pmatrix}
\cdot
\begin{pmatrix}
a_{1}\\
\vdots\\
a_{n}
\end{pmatrix}
\end{align*}$$
Where the columns of the first are each $[Tv_{i}]$ with coordinates in $\beta$, and the right in just the coordinates of $[v]_{\alpha}$, and the first is denoted by $[T]^{\alpha}_{\beta}$, the matrix will be $m \times n$ where:
- $m$ is the dimension of the [[Range in Discrete Math|range]] $W$
- $n$ is the [[Theorems and Proofs for Basis and Dimension|dimension]] of the [[Domain]] $V$ 
___
## Application
Let $T:\mathbb{R}^{3} \rightarrow \mathbb{R}^{2}$,  given by $S(x,y,z) = (x+y+z, x-y+z)$, and Let $\alpha = \{(1,0,1), (1,1,0), (2,1,0)\}$, $\beta = \{(2,1), (1,2)\}$ be [[Theorems and Proofs for Basis and Dimension|basis]].
Find $[S]^{\alpha}_{\beta}$, let $[v]_{\alpha}=\begin{pmatrix}2\\-4\\3\end{pmatrix}$, find $[S(v)]_{\beta}$.
So we're going to:
- Find the image of each vector of $\alpha$.
- Find a generical representation of $\beta$ over some $(x,y)$ vector.
- Write every [[Image of a linear transformation|image]] in $\beta$ coordinates
- Put each in a column, and we have $[S]^{\alpha}_{\beta}$.

The images are:
$$\begin{align*}
S(1,0,1) &= (2,2)\\
S(1,1,0) &= (2,0)\\
S(2,1,0) &= (3,1)
\end{align*}$$
The generical representation will go like:
$$\begin{align*}
(x,y) &= a(2,1)+b(1,2)\\
(x,y)&= (2a+b, a+2b)\\\\
&\begin{pmatrix}
2 & 1 & \mid & x\\
1 & 2 & \mid & y
\end{pmatrix}
\implies
\begin{pmatrix}
1 & 0 & \mid & \frac{2x-y}{3}\\
0 & 1 & \mid & \frac{2y-x}{3}
\end{pmatrix}
\end{align*}$$
Hence the coordinates of a generical vector $(x,y)$ in $\beta$ is:
$$\begin{align*}
[(x,y)]_{\beta}=\begin{pmatrix}\frac{2x-y}{3}\\ \frac{2y-x}{3}\end{pmatrix}
\end{align*}$$
Finding every image in $\beta$ coordinates:
$$\begin{align*}
[(2,2)]_{\beta}&= \begin{pmatrix} \frac{2}{3} \\ \frac{2}{3} \end{pmatrix}\\
[(2,0)]_{\beta}&= \begin{pmatrix} \frac{4}{3}\\ \frac{-2}{3} \end{pmatrix}\\
[(3,1)]_\beta &= \begin{pmatrix} \frac{5}{3} \\ \frac{-1}{3} \end{pmatrix}
\end{align*}$$
Therefore:
$$\begin{align*}
[S]^{\alpha}_{\beta}=\frac{1}{3} \begin{pmatrix}
2 & 4 & 5\\
2 & -2 & 1
\end{pmatrix}
\end{align*}$$
and:
$$\begin{align*}
[S(v)]_{\beta}&= [S]^{\alpha}_{\beta}\cdot [v]_{\beta}\\
&= \frac{1}{3}\begin{pmatrix}2 & 4 & 5\\
2 & -2 & -1\end{pmatrix} \begin{pmatrix}2\\-4\\3\end{pmatrix}\\
&= \begin{pmatrix}1\\3\end{pmatrix}
\end{align*}$$
$\rm{Q.E.D}$.