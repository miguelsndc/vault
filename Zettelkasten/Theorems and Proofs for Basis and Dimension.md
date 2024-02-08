---
tags: spaces
---
Let $V$ be a [[Vector Space]], a set of vectors $S = \{v_{1},v_{2},\cdots, v_{n}\}$ is called a **basis** of $V$ [[If and Only if]] $\span(S) = V$ and $S$ is [[Linear (In)dependence.|linearly independent]]. The **dimension** of a vector space is the number of elements in the basis. if $\dim(V) = n$ and $S$ is a basis of $V$, then $|S| = n$. 

>Theorem: Let $v_{1},v_{2},\cdots,v_{n}$ be non-null vectors that span a space $V$. Then, among those vectors we can extract a basis for $V$.

## Proof:
If $v_{1}, v_{2}, \cdots, v_{n}$ are [[Linear (In)dependence.|linearly]] independent, they form a basis and we're done. If they aren't, then there is some [[Linear Combinations|linear combination]] of them, with non-zero coefficients that yields $\vec{0}$. Suppose that $x_{n} \ne 0$ then we can write $v_{n}$ in terms of the other $n-1$ [[Vector|vectors]] as such:
$$\begin{align*}
x_{1}v_{1}+x_{2}v_{2}+\cdots+x_{n}v_{n}&=0 \text{ Suppose xn is non-zero}\\
x_{n}v_{n}&=-x_{1}v_{1}+(-x_{2})v_{2}+\cdots+(-x_{n-1})v_{n-1}\\
v_{n}&= \left(\frac{-x_{1}}{x_{n}}\right)v_{1}+\left(\frac{-x_{2}}{x_{n}}v_{2}\right)+\cdots+ \left(\frac{-x_{n-1}}{x_{n}}\right)v_{n-1}
\end{align*}$$
If $v_{1}, \cdots, v_{n-1}$ is linearly **de**pendent, then there is a vector that is a linear combination of them, we can extract this vector like we did, and keeping doing this, after a **finite** amount of steps we reach a subset of $\{v_{1},\cdots,v_{n}\}$ with $r$ independent vectors ($r\le n$), $v_{i1},v_{i2},\cdots,v_{ir}$ that still span $V$. and they are form a basis. 

> Theorem: Let $V$ be a vector space spanned by a finite set of vectors $v_{1},v_{2},\cdots, v_{n}$. Then, any set with more than $n$ vectors is automatically linearly **dependent** (And, therefore, any linearly **independent** set has at most $n$ vectors)>

Since $\span(v_{1},v_{2}, \cdots, v_{n}) = V$, by the previous theorem we can extract a basis from it, Let $v_{1}, v_{2}, \cdots, v_{r}, r\le n$ be that basis. Consider now $w_{1}, w_{2}, \cdots, w_{n}$, $m$ vectors from $V$, with $m \gt n$. Then, there exists [[Scalar|scalars]] $a_{ij}$, such that:
$$(I) \;\;\; \begin{cases}
w_{1}= a_{11}v_{1}+a_{12}v_{2}+ \cdots a_{1r}v_{r}\\
w_{2}= a_{21}v_{1}+a_{22}v_{2}+ \cdots a_{2r}v_{r}\\
\vdots\\
w_{m}= a_{m1}v_{1}+a_{m2}v_{2}+ \cdots a_{mr}v_{r}
\end{cases}$$
Now suppose a linear combination of $w_{1}, \cdots, w_{m}$ giving $\vec{0}$:
$$(II)\;\;\;\begin{align*}
x_{1}w_{1}+x_{2}w_{2}+\cdots+x_{m}w_{m}&= \vec{0}
\end{align*}$$
Now substituting and collecting terms from the substitution of $I$ in $II$ we get:
$$\begin{align*}
\vec{0} &= 
(a_{11}x_{1}+a_{21}x_{2}+\cdots+a_{m1}x_{m})v_{1}+\\
&+(a_{12}x_{1}+a_{22}x_{2}+\cdots+a_{m2}x_{m})v_{2}+ \cdots\\
&+ (a_{1r}x_{1}+a_{2r}x_{2}+ \cdots +a_{mr}x_{m})v_{r}\\
\end{align*}$$
Since $v_{1}, v_{2}, \cdots, v_{r}$ are $\rm{L.I}$ then:
$$\begin{align*}
\begin{cases}
a_{11}x_{1}+a_{21}x_{2}+\cdots+a_{m1}x_{m} &= 0\\
a_{12}x_{1}+a_{22}x_{2}+\cdots+a_{m2}x_{m}&= 0\\
\vdots\\
a_{1r}x_{1}+a_{2r}x_{2}+ \cdots +a_{mr}x_{m}&= 0
\end{cases}
\end{align*}$$
We now have a [[Homogeneous System]] with $r$ equations and $m$ unknowns, and since $r \le n \lt m$ than, it admits a non-trivial solution, that menns, there is a solution for some $x_{i}$ non-zero, therefore $w_{1}, w_{2}, \cdots, w_{m}$ are $\rm{L.D}$.

> Theorem: Any basis of a vecotr space always got the same number of elements. This number is called the **dimension** of $V$, denoted by $\dim(V)$.

## Proof
Let $\{v_{1}, v_{2}, \cdots, v_{n}\}$ and $\{w_{1}, w_{2}, \cdots, w_{n}\}$ be a basis for $V$. By the previous theorem, since $\span(\{v_{1}, v_{2}, \cdots, v_{n}\}) = V$ and $w_{1}, w_{2}, \cdots, w_{m}$ is $\rm{L.I}$, then $m \le n$. However, since $\span(\{w_{1}, w_{2}, \cdots, w_{m}\})=V$ and $v_{1}, v_{2}, \cdots, v_{n}$ is $\rm{L.I}$, then $n \le m$. Therefore $n = m$.

