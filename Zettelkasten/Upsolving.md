$$
\begin{align*}
T(x,y,z)&=(2x+y-z,x+y+z,x+y+z)\\
\alpha &= \{(0,0,1),(0,1,1),(1,1,1)\}\\\\
(1,0,0)&= a(0,0,1)+b(0,1,1)+c(1,1,1)\\
(0,1,0)&= a(0,0,1)+b(0,1,1)+c(1,1,1)\\
(0,0,1)&= a(0,0,1)+b(0,1,1)+c(1,1,1)\\\\
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

$$\begin{align*}
[S]^{\alpha}_{\alpha} &= \begin{pmatrix}2 & 3 \\1 & -5\end{pmatrix}\;\alpha= \{(1,1),(1,2)\}\\\\
[S]^{\alpha}_{\gamma}&=I \\
[S]^{\alpha}_{\gamma}&=[I]^{\alpha}_{\gamma}\cdot[S]^\alpha_{\alpha} \implies[I]^{\alpha}_{\gamma}=([S]^\alpha_{\alpha})^{-1}\\\\
([S]^{\alpha}_{\alpha})^{-1}&= \begin{pmatrix}
\frac{5}{13} & \frac{3}{13}\\
\frac{1}{13} & \frac{-2}{13}
\end{pmatrix}= [I]^{\alpha}_{\gamma}\\
[(1,1)]_{\gamma}&= \frac{5}{13}\cdot v_{1} + \frac{1}{13}\cdot v_{2}\\
[(1,2)]_{\gamma}&= \frac{3}{13}\cdot v_{1}  -\frac{2}{13}\cdot v_{2}\\
(3,4) &= v_{1}\\
(-2,-7)&= v_{2}
\end{align*}$$
$$\begin{align*}
&T(a_{0}+ a_{1}x+a_{2}x^{2})= (a_{0}+a_{1}, a_{0} - a_{1} -a_{2}, a_{1}+2a_{2})\\
&\alpha =\{1,x,x^{2}\}\;\;\beta =\{(1,0,1),(1,0,0),(0,1,1)\}\\\\
[(x,y,z)]_{\beta}&= \begin{pmatrix}z-y \\ x-z+y\\ y\end{pmatrix}\\\\
T(1)&= (1,1,0) \rightarrow (-1,2,1)_{\beta}\\
T(x)&= (1,-1,1) \rightarrow (0,-1,-1)_{\beta}\\
T(x^{2})&= (0,0,2) \rightarrow (2,-2,0)_{\beta}\\\\
&[T]^{\alpha}_{\beta}\begin{pmatrix}
-1 & 0 & 2\\
2 & -1 & -2 \\
1 & -1 & 0
\end{pmatrix}\rightarrow2^{2}+(-1)^{2}+(-2)^{2}=9
\end{align*}$$$$\begin{align*}
T^{\textrm{QUALQUER COISA}}_{\textrm{QUALQUER COISA}}&= [I]^\beta_{\textrm{QUALQUER COISA}}\cdot T^{\alpha}_{\beta}\cdot[I]_{\alpha}^{\textrm{QUALQUER COISA}}
\end{align*}$$
