Let $T:V \rightarrow W$ be a [[Bijective Linear Transformations|bijective]] [[Linear Transformations|linear transformation]], Let $\alpha = \{v_{1},v_{2}, \cdots, v_{n}\} \subset V$ be a [[Theorems and Proofs for Basis and Dimension|basis]]of the [[Domain]] $V$. then $\{Tv_{1},\cdots, Tv_{n}\}$ is a [[Span|spanning set]] of the [[Image of a linear transformation|image]] of $T$. From the theorem that [[Injective transformations preserve independence]], $\{Tv_{1},\cdots Tv_{n}\}$ is also a [[Theorems and Proofs for Basis and Dimension|basis]] of the [[Image of a linear transformation|image]].
Since $T$ is [[Surjective Functions|surjective]], $\im(T)=W$, therefore $\{Tv_{1}, \cdots, Tv_{n}\}$ is a [[Theorems and Proofs for Basis and Dimension|basis]] of the [[Range]] $W$.
Notice that $\dim(V) = \dim(W) = n$ for $T$ to be invertible.
___
Notation: $T: V \rightarrow W \implies T^{-1}:W \rightarrow V$.
$$\begin{align*}
T^{-1}(Tv_{1}) &= v_{1}\\
\vdots\\
T^{-1}T(v_{n})&= v_{n}
\end{align*}$$
Consider $v\in V: v=a_{1}v_{1}+\cdots+a_{n}v_{n}$, hence:
$$\begin{align*}
Tv&= a_{1}Tv_{1} +\cdots+a_{n}Tv_{n}\\
T^{-1}T(v) &= T^{-1}(a_{1}Tv_{1} + \cdots+a_{n}Tv_{n})\\
&= a_{1}T^{-1}T_{v1}+\cdots+a_{n}T^{-1}Tv_{n}\\
&= a_{1}v_{1}+ \cdots + a_{n}v_{n}\\
&= v
\end{align*}$$
Hence the [[Composition of Linear Transformations|composition]] $T^{-1}\circ Tv = v$, also $T^{-1} \circ T= I$, $I$ is the **identity** transformation. A $L.T$ that preserves all [[Vector|vectors]].
___
## How to find it
Let $T: \mathbb{R^{3}} \rightarrow P_{2}$, given by: $T(x-y-z) = (x-y) + (2x-z)X+(x-y-z)X^{2}$.
1. Step 1: Show $T$ is bijective. We can do this by finding [[Kernel of a linear transformation|kernel]] or the [[Image of a linear transformation|image]] of $T$, and if $\dim(\im(T)) = 3 = \dim(P_{2}) \implies \dim(\nu(T)) = 0$, hence $T$ is [[Bijective]] or the other way around. both work. finding both is unnecessary.
2. Step 2: Find the inverse:
Remember we can [[Find the law of a transformation through a basis and some results]], we can find some results of+  $T$ itself through a [[Theorems and Proofs for Basis and Dimension|basis]], most convinently the [[Canonical Vectors|canonical]] basis. So:
$$\begin{align*}
T(1,0,0) &= 1+2X+X^{2}\\
T(0,1,0)&= -1-X^{2}\\
T(0,0,1)&= -X-X^{2}
\end{align*}$$
Therefore:
$$\begin{align*}
T^{-1}(1+2X+X^{2})&= (1,0,0)\\
T^{-1}(-1-X^{2})&= (0,1,0)\\
T^{-1}(-X-X^{2})&= (0,0,1)
\end{align*}$$
We can now put all this in a big [[Matrix Definition|matrix]] with the inputs and the images side by side, and find the [[Inverse Matrix]]:
$$\begin{align*}
\begin{pmatrix}
1 & 2 & 1 & \mid & 1 & 0 & 0 \\
-1 & 0 & -1 & \mid & 0 & 1 & 0 \\
0 & -1 & -1 & \mid & 0 & 0 & 1
\end{pmatrix}
\end{align*}$$
In [[Row Reduced Echelon Form]] it becomes:
$$\begin{align*}
\begin{pmatrix}
1 & 0 & 0 & \mid & \frac{1}{2}& \frac{-1}{2} & 1\\
0 & 1 & 0 & \mid & \frac{1}{2} & \frac{1}{2} & 0\\
0 & 0 & 1 & \mid & \frac{-1}{2} & \frac{-1}{2} & -1
\end{pmatrix}
\end{align*}$$
The [[Matrix Definition|matrix]] on the right side is the [[Transposes|transpose]] of the [[Matrix Definition|matrix]] that represents $T^{-1}$, so the expression is defined by:
$$\begin{align*}
\frac{1}{2}\begin{pmatrix}
1 & 1 & -1\\
-1 & 1 & -1 & \\
2 & 0 & -2
\end{pmatrix}
\begin{pmatrix}
a_{0}\\
a_{1}\\
a_{2} 
\end{pmatrix}
&= \frac{1}{2}(a_{0} +a_{1}-a_{2}, -a_{0}+a_{1}-a_{2}, 2a_{0}-2a_{2})
\end{align*}$$
Therefore:
$$\begin{align*}
T^{-1}(a_{0} + a_{1}X + a_{2}X^{2})=\frac{1}{2}(a_{0} +a_{1}-a_{2}, -a_{0}+a_{1}-a_{2}, 2a_{0}-2a_{2})
\end{align*}$$
