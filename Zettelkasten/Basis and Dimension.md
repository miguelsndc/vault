---
tags: spaces
---
Let $V$ be a [[Vector Space]], a set of vectors $S = \{v_{1},v_{2},\cdots, v_{n}\}$ is called a **basis** of $V$ [[If and Only if]] $\span(S) = V$ and $S$ is [[Linear (In)dependence.|linearly independent]]. The **dimension** of a vector space is the number of elements in the basis. if $\dim(V) = n$ and $S$ is a basis of $V$, then $|S| = n$. 

>Theorem: Let $v_{1},v_{2},\cdots,v_{n}$ be non-null vectors that span a space $V$. Then, among those vectors we can extract a basis for $V$.

Proof:
If $v_{1}, v_{2}, \cdots, v_{n}$ are [[Linear (In)dependence.|linearly]] independent, they form a basis and we're done. If they aren't, then there is some [[Linear Combinations|linear combination]] of them, with non-zero coefficients that yields $\vec{0}$. Suppose that $x_{n} \ne 0$ then we can write $v_{n}$ in terms of the other $n-1$ [[Vector|vectors]] as such:
$$\begin{align*}
x_{1}v_{1}+x_{2}v_{2}+\cdots+x_{n}v_{n}&=0 \text{ Suppose xn is non-zero}\\
x_{n}v_{n}&=-x_{1}v_{1}+(-x_{2})v_{2}+\cdots+(-x_{n-1})v_{n-1}\\
v_{n}&= \left(\frac{-x_{1}}{x_{n}}\right)v_{1}+\left(\frac{-x_{2}}{x_{n}}v_{2}\right)+\cdots+ \left(\frac{-x_{n-1}}{x_{n}}\right)v_{n-1}
\end{align*}$$
If $v_{1}, \cdots, v_{n-1}$ is linearly **de**pendent, then there is a vector that is a linear combination of them, we can extract this vector like we did, and keeping doing this, after a **finite** amount of steps we reach a subset of $\{v_{1},\}$