---
tags: eigen-everything
aliases: eigen, eigenvalue, eigenvalues, eigenvector, eigenvectors
---
A rotation $R_{\theta}$ is a [[Linear maps|linear map]] of $\mathbb{R^{3}}$ where the [[Vector|vectors]] rotate through an axis $t$ by an angle $\theta$. However, if we apply the rotation to a vector in the axis $t$, it won't direction at all. Such vectors $v$ when applied some transformation $T$ that **do not change direction** and are **only scaled by a factor $\lambda$** are called ***eigenvectors***, and the [[Scalar|scalars]] $\lambda$ are called the ***eigenvalues***. 
Eigen's are associated to a [[Linear Transformations|transformation]], each transformation has one, many or **no** eigen's at all.
## Definition
Let $T:V \rightarrow V$ be a [[Linear maps|linear map]], we say that $v \ne \vec{0}$ is a [[Eigenvalues and Eigenvectors|eigenvector]] of $T$ if exists $\lambda \in \mathbb{R}$ such that $T(v) = \lambda v$. Where $\lambda$ is called the *eigenvalue* of $v$.
Let $V = \mathbb{R}^{2}$ and $T(x,y) = (2x+y, x-y)$. By the definition, we'll have the expression:
$$\begin{align*}
T(x,y) &= \lambda v\\
(2x+y,x-y)&= \lambda(x,y)
\end{align*}$$
Here we have three unknows, $\lambda$, the eigenvalue, $x$, and, $y$. Treat $\lambda$ as a constant, (it actually is):
$$\begin{align*}
(2x+y,x-y) &= \lambda(x,y)\\
&\begin{cases}
2x+y&= \lambda x\\
x-y&= \lambda y
\end{cases}\\
&\begin{cases}
2x+y- \lambda x&= 0\\
x-y- \lambda y&= 0
\end{cases}\\
&\begin{cases}
(2-\lambda)x+y=0\\
x+(-1-\lambda)y=0
\end{cases}
\end{align*}$$
Notice we need $v \ne 0$ so it can be an eigenvector, so we **are not interested in systems with unique solutions**, we're gonna solve the system trying to force it to have **infinetely many** solutions:
$$\begin{align*}
\begin{pmatrix}2-\lambda & 1\\
1 & -1-\lambda\end{pmatrix} \implies
\begin{pmatrix}
 1 & -1-\lambda\\
0 & (\lambda - 2)(-1 - \lambda)+1 
\end{pmatrix}
\end{align*}$$
So, to have infintely many solutions, $T_{2,2}$ needs to equal zero, so:
$$
\begin{align*}
(\lambda -2)(- 1 - \lambda) + 1 &= 0\\
-\lambda^{2} + \lambda + 3 &= 0\\
\lambda^{2} - \lambda -3&= 0
\end{align*}
$$
Solutions are: $\{\frac{1+\sqrt(13)}{2}, \frac{1 - \sqrt(13)}{2} \}$. So this is the eigenvalue [[Sets|set]]. To find the eigenvectors associated, we replace $\lambda$ in the system by these values one by one and find it. However, one can take advantage of [[Matrix Definition|matrices]] .
## Matrix Definition
Suppose $T:V \rightarrow V$ is a [[Linear maps|linear map]]. Let $\alpha$ be a [[Theorems and Proofs for Basis and Dimension|basis]] of $V$. Hence, the matrix $[T]^{\alpha}_{\alpha}$ is a [[Square Matrix]]. A vector $[T(v)]_{\alpha} = [T]^{\alpha}_{\alpha} \cdot [v]_{\alpha}$. Let $A = [T]^{\alpha}_{\alpha}$ and $v = [v]_{\alpha}$. Suppose now $v \ne \vec{0}$ is an eigenvector of $T$ (eigenvector of $A$), therefore:
$$\begin{align*}
Av&= \lambda v, \;\;\; \lambda \in \mathbb{Rr}\\
Av - \lambda v&=  0
\end{align*}$$
One might be tempted to factor $v$, however, $\lambda$ is a [[Scalar|scalar]] and $A$ is a [[Matrix Definition|matrix]], we can't do that. However, $Iv = v$, where $I$ is the [[Identity Matrix]], so we can use this little hack to solve our problem:
$$\begin{align*}
Av- \lambda v&= 0\\
Av- \lambda Iv&= 0\\
v(A-\lambda I) &= 0 
\end{align*}$$
$A$ is a $n \times n$ square matrix, then $I$ must be the $n \times n$ identity. And notice this also is a [[Homogeneous System]], and that's exactly the system we want to have infinetly many solutions.
The matrix $A - \lambda I$ needs to be non-inversible, If it is, then:
$$\begin{align*}
P &= 0\\
P^{-1}P&= P^{-1}\cdot 0\\
I&= 0
\end{align*}$$
And it has unique solutions. One key factor is: if the determinant of a matrix equals zero, it doesn't have an inverse. We'll use this restriction to force what we want, see:
$$\begin{align*}
A^{-1}A&= I\\
\det(A^{-1}A)&= \det(I) = 1\\
\det(A^{-1})\cdot \det(A)&= 1\\
\det(A^{-1})&= \frac{1}{\det(A)}
\end{align*}$$
So, to admit eigenvectors, the determinant must equal zero, so the above expression has no solutions.
The eigenvectors are the roots of the [[Polynomials|polynomial]] $\det(A-\lambda I)$. This polynomial is called the **characteristic polynomial** of $A$ and of $T$. So, an example is:
For $T(x,y,z)=(2x-y+z,x-z,3x-y)$ find the eigenvalues/vectors.
$$\begin{align*}
[T]^{\epsilon}_{\epsilon}&= \begin{pmatrix}
2 & -1 & 1 \\
1 & 0 & -1 \\
3 & -1 & 0 
\end{pmatrix}\\
\begin{pmatrix}
2 & -1 & 1 \\
1 & 0 & -1 \\
3 & -1 & 0 
\end{pmatrix} - \begin{pmatrix}
\lambda  & 0 & 0\\
0 & \lambda & 0\\
0 & 0 & \lambda
\end{pmatrix}&\implies \begin{pmatrix}
2 - \lambda  & -1 & 1\\
1 & -\lambda & -1\\
3 & -1 & -\lambda
\end{pmatrix} 
\end{align*}$$
So:
$$\begin{align*}
\det(A - \lambda I) =0 \implies \det\begin{pmatrix}
2 - \lambda  & -1 & 1\\
1 & -\lambda & -1\\
3 & -1 & -\lambda
\end{pmatrix}=0
\end{align*}$$
So after calculating determinants with whatever method, the expression becomes $\lambda(\lambda^{2}-2\lambda -3)=0$ , the inner expression can be factored into $(\lambda + 1)(\lambda - 3) = 0$, So the eigenvalues are $\{0, -1, 3\}$. Replace $\lambda$ in the $A - \lambda I$ to find the 