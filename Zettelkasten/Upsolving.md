$$
\begin{align*}
T(x,y,z)&=(2x+y-z,x+y+z,x+y+z)\\
\alpha &= \{(0,0,1),(0,1,1),(1,1,1)\}\\\\
(1,0,0)&= a(0,0,1)+b(0,1,1)+c(1,1,1)\\
(0,1,1)&= a(0,0,1)+b(0,1,1)+c(1,1,1)\\
(1,1,1)&= a(0,0,1)+b(0,1,1)+c(1,1,1)\\\\
(x,y,z)&= a(0,0,1)+b(0,1,1)+c(1,1,1)\\\\
&\begin{pmatrix}
0 & 0 & 1&x \\
0 & 1 & 1&y \\
1 & 1 & 1&z
\end{pmatrix}\rightarrow
\begin{pmatrix}
1 & 0 & 0 & z-y\\
0 & 1 & 0 & y-x\\
0 & 0 & 1 & x
\end{pmatrix}\\\\
&[(x,y,z)]_{\alpha}=\begin{pmatrix}z-y\\ y-x\\x\end{pmatrix}\rightarrow
\begin{cases}
T(1,0,0)&= (2,1,-1)\\ 
T(0,1,0)&= (1,1,1)\\
T(0,0,1)&= (1,1,1)\\
\end{cases}
\rightarrow
\begin{cases}
[(2,1,-1)]_{\alpha}=\begin{pmatrix}-2 & -1 & 2\end{pmatrix}^{T}\\
[(1,1,1)]_{\alpha}=\begin{pmatrix}0 & 0 & 1\end{pmatrix}^{T}\\
[(1,1,1)]_{\alpha}=\begin{pmatrix}0 & 0 & 1\end{pmatrix}^{T}\\\\
\end{cases}\\
&\therefore [T]^{\epsilon}_{\alpha}= \begin{pmatrix}
-2 & 0 & 0 \\
-1 & 0 & 0 \\
2 & 1 & 1
\end{pmatrix} \rightarrow 2 +2+1+1+1=7
\end{align*}
$$
$$\begin{align*}
[T]^{x}_{y}=\begin{pmatrix}
[T(x_{1})]_{y} & [T(x_{2})_{y}]\dots[T(x_{n})_{y}]
\end{pmatrix}
\end{align*}$$
