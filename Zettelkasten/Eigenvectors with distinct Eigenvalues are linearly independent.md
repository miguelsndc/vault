---
tags: eigen-everything
---
Let $\lambda_{1}$ and $\lambda_{2}$ be [[Eigenvalues and Eigenvectors|eigenvalues]] of a [[Linear maps|linear map]] $T$ in a [[Vector Space|space]] $V$ with $\lambda_{1}\ne \lambda_{2}$. Let $v_1$ and $v_{2}$ be the associated [[Eigenvalues and Eigenvectors|eigenvectors]].
So, let $a_{1}v_{1}+a_{2}v_{2}=\vec{0}$, let us apply $T - \lambda_{2} I$ to this [[Equation]], then we obtain:
$$\begin{align*}
T-\lambda_{2}I(a_{1}v_{1}+a_{2}v_{2})&= 0\\
T-\lambda_{2}I(a_{1}v_{1}) + T-\lambda_{2}I(a_{2}v_{2})&= 0 \\
a_{1}\cdot T - \lambda_{2}I (v_{1}) + a_{2}T- \lambda_{2}I(v_{2}) &= 0\\
a_{1}(T(v_{1})- \lambda_{2}v_{1})+ a_{2}(T(v_{2}) - \lambda_{2}v_{2})&= 0\\
a_{1}(\lambda_{1}v_{1} - \lambda_{2}v_{1}) + a_{2}(\lambda_{2}v_{2} - \lambda_{2}v_{2})&= 0\\
a_{1}(\lambda_{1}- \lambda_{2})v_{1} + a_{2}(\lambda_{2} - \lambda_{2})&= 0 
\end{align*}$$
Since $a_{2}(\lambda_{2} - \lambda_{2}) = 0$, we get $a_{1}(\lambda_{1}- \lambda_{2})v_{1} = 0$. Since $\lambda_{1} \ne \lambda_{2}$ and $v_{1} \ne 0$, it follows that $a_{1} = 0$. From applying $T - \lambda_{1}I$ to the original equation we obtain:
$$\begin{align*}
a_{1}(\lambda_{1} - \lambda_{1})v_{1}+ a_{2}(\lambda_{2} - \lambda_{1})v_{2}
&= 0\end{align*}$$