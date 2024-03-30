---
tags: matrix, vector, spaces
---
Let $V$ be a [[Vector Space|vector space]] with [[Inner Product|inner product]] $\innp{,}$. The operation of taking the inner product can be expressed as [[Matrix Multiplication|matrix multiplication]], as we'll see.

Let $\alpha = \{v_{1},v_{2}, \cdots, v_{n}\}$ a arbitrary [[Theorems and Proofs for Basis and Dimension|basis]] of $V$, let $u,v \in V$, then:
$$\begin{align*}
u &= a_{1}v_{1}+a_{2}v_{2}+\cdots+a_{n}v_{n}\\
v&=b_{1}v_{1}+b_{2}v_{2} + \cdots+b_{n}v_{n}\\\\
\innp{u,v}&= \innp{
a_{1}v_{1}+a_{2}v_{2}+\cdots+a_{n}v_{n},
b_{1}v_{1}+b_{2}v_{2} + \cdots+b_{n}v_{n}
}\\
&= a_{1}b_{1}\innp{v_{1},v_{1}}+\cdots+a_{1}b_{n}\innp{v_{1},v_{n}}+a_{2}b_{1}\innp{v_{2},v_{1}}+ a_{2}b_{2}\innp{v_{2},v_{2}}+\cdots+
\end{align*}$$