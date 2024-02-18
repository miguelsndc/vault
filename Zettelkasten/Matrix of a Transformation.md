---
tags: linear-transformations
---
Consider $T:V \rightarrow W$ [[Linear Transformations|linear transformation]] and two [[Theorems and Proofs for Basis and Dimension|basis]] $\alpha=\{v_{1},\cdots, v_{n}\}, \beta = \{w_{1},\cdots, w_{n}\}$ where $\dim{V} = n$ and $\dim{W} = m$,
Let $v \in V$, so $v$ can be written as $v= a_{1}v_{1} + \cdots + a_{n}v_{n}$, after applying $T$, we obtain $Tv = a_{1}Tv_{1}+ \cdots + a_{n}Tv_{n}$. 
We want to find $[w]_{\beta} = [Tv]_{\beta}$.
- Note that if $\{Tv_{1}, \cdots, Tv_{n}\}$ was a [[Theorems and Proofs for Basis and Dimension|basis]], $\gamma$, then $[Tv]_{\gamma} = \begin{pmatrix}a_{1}\\ \vdots \\ a_{n}\end{pmatrix}$, the actual coefficients of $v$, since transformations preserve the [[Coordinates]], however, this happens [[If and Only if|if and only if]] $T$ is a [[Isomorphism]], if it's not, then the [[Image of a linear transformation|image]] doesn't form a [[Theorems and Proofs for Basis and Dimension|basis]] therefore the coordinates aren't exactly the same.

Write each $Tv_{i}$ as a [[Linear Combinations|linear combination]] of $\beta$:
$$\begin{align*}
\begin{cases}
Tv_{1}=a_11
\end{cases}
\end{align*}$$