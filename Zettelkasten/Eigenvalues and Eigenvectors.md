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
\begin{cases}
2x+y&= \lambda x\\
x-y&= \lambda y
\end{cases}
\end{align*}$$