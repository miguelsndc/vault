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
&= a_{1}b_{1}\innp{v_{1},v_{1}}+\cdots+a_{1}b_{n}\innp{v_{1},v_{n}}+a_{2}b_{1}\innp{v_{2},v_{1}}+ a_{2}b_{2}\innp{v_{2},v_{2}}+\cdots+a_{n}b_{n}\innp{v_{n},v_{n}}
\end{align*}$$
By paying enough attention, one can see that this is the multiplication of the [[Vector Coordinates|coordinates]] of $u$, a [[Square Matrix]], and the coordinates of $v$, notice:
$$\begin{align*}
\begin{pmatrix}
\innp{v_{1},v_{1}} & \cdots & \innp{v_{1},v_{n}}\\
\innp{v_{2},v_{1}} & \cdots & \innp{v_{2},v_{n}}\\
\vdots &   & \vdots\\
\innp{v_{n},v_{1}} & \cdots & \innp{v_{n},v_{n}}\\
\end{pmatrix}
\cdot
\begin{pmatrix}
b_{1} \\ \vdots \\ b_{n}
\end{pmatrix}
\end{align*}$$
Which results in:
$$\begin{align*}
\begin{pmatrix}
\innp{v_{1},v_{1}}b_{1} + \cdots+\innp{v_{1},v_{n}}b_{n}\\
\innp{v_{2},v_{1}}b_{1} + \cdots+\innp{v_{2},v_{n}}b_{n}\\
\vdots\\
\innp{v_{n},v_{1}}b_{1} + \cdots+\innp{v_{n},v_{n}}b_{n}
\end{pmatrix}
\end{align*}$$
which is then multiplied by the coordinates of $u$ [[Transposes|transpose]], just for it to work properly:

$$
\begin{pmatrix}a_{1} & a_{2} & \cdots & a_{n}\end{pmatrix}
\begin{pmatrix}
\innp{v_{1},v_{1}}b_{1} + \cdots+\innp{v_{1},v_{n}}b_{n}\\
\innp{v_{2},v_{1}}b_{1} + \cdots+\innp{v_{2},v_{n}}b_{n}\\
\vdots\\
\innp{v_{n},v_{1}}b_{1} + \cdots+\innp{v_{n},v_{n}}b_{n}
\end{pmatrix}
$$
Which results in a [[Real Numbers|real number]], the actual inner product, this operation can be generalized to the following:
$$\begin{align*}
\innp{u,v}&= ([u]_{\alpha})^{T}\cdot G_{\alpha}\cdot[v]_{\alpha} 
\end{align*}$$
Where $G_{\alpha}$ is the **inner product matrix**. Notice the inner p. is always the same regardless of the basis.