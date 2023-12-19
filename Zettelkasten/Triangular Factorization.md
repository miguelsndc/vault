---
tags: systems
---
Do [[Gaussian Elimination]] on a $Ax = b$ [[Definition of a System of Linear Equations|system]] creates a new system $Ux = c$, where $U$ is $A$ in [[Upper Triangular Matrix|upper triangular form]], $c$ is the new [[Vector|vector]] derived from $b$ by the same steps that took $A$ into $U$.
See an example:
$$\begin{align*}
Ax = \begin{pmatrix}
2 & 1 & 1\\
4 & 1 & 0\\
-2 & 2 & 1
\end{pmatrix}
\begin{pmatrix}
u\\
v\\
w\\
\end{pmatrix} = \begin{pmatrix}
1\\
-2\\
7\end{pmatrix}
\end{align*}$$
Then there's three elimination steps:
1. Subtract $2$ times the first equation from the second;
2. Subtract $-1$ times the first equation from the third (add);
3. Subtract $-3$ times the second equation from the third (add);
The result is the equivalent:
$$\begin{align*}
Ux = \begin{pmatrix}
2 & 1 & 1\\
0 & -1 & 0\\
0 & 0 & -4
\end{pmatrix}
\begin{pmatrix}
u\\
v\\
w\\
\end{pmatrix} = \begin{pmatrix}
1\\
-4\\
-4\end{pmatrix}
\end{align*}$$
There's the $Ux = c$ 