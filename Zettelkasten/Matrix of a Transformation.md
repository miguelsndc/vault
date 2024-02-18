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

\end{pmatrix}
\end{align*}$$