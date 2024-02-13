---
tags: linear-transformations
---
In case of [[Functions]] in general, [[Strategies to Prove Surjectivity|surjectivity]] is defined as: Let $f: A \rightarrow B$, then if is surjective if and only if $\forall b \in B \;\; \exists a \in A \mid f(a) = b$. When talking about [[Linear Transformations]], surjectivity is defined through the [[Image of a linear transformation|image]]: 
Let $T:V \rightarrow W$ be a linear transformation, $T$ is surjective [[If and Only if|if and only if]], $\im(T) =W$, since $\im(T) \subset W$, if the [[Theorems and Proofs for Basis and Dimension|dimension]] of $W$ and $\im(T)$ are the same then $\im(T) = W$. ($\dim[\im(T)] = \dim(W)$.
So let $\{v_{1},v_{2},\cdots, v_{n}\}$ be a [[Theorems and Proofs for Basis and Dimension|basis]] of $\im(T)$, (since the image is a [[Linear Subspaces|subspace]].) if $n = \dim(W)$, then ${v_{1}, v_{2},\cdots, v_{n}}$ is also a [[Theorems and Proofs for Basis and Dimension|basis]] for $W$ and hence $\im(T) = W$ since the [[Span|span]] of both cover the same [[Linear Subspaces|subspace]].
## How to find it
We want to know whether the [[Theorems and Proofs for Basis and Dimension|dimension]] of both $\im(T)$ and $W$ on $T:V \rightarrow W$, are the same, so, when defining a [[Linear Transformations|linear transformation]] we usually know which space it's being mapped to which space, therefore knowing it's dimension. Therefore, simply finding a [[Theorems and Proofs for Basis and Dimension|basis]] for $\im(T)$ will do the job, and if the number of elements in the basis of $\im(T)$ is equal to the dimension of $W$ then they are the same hence $T$ is [[Surjective Functions|surjective]].
$\rm{Example}:$ 
Let $T:P_{2}\rightarrow \mathbb{R}^{3}$ : $T(a_{0}+a_{1}X +a_{2}X^{2}) = (a_{0}-a_{2}, a_{1}+a_{2}, a_{0}+ a_{1})$
$\im(T) = \{(x,y,z) \in \mathbb{R}^{3} \mid T(a_{0} + a_{1}X + a_{2}X^{2}) = (x,y,z) \}$, for some $(a_{0} + a_{1}X + a_{2}X^{2}) \in P_{2}$.
$(a_{0}-a_{2}, a_{1}+a_{2}, a_{0}+ a_{1}) = (x,y,z) \implies a_{0}(1,0,1) + a_{1}(0,1,1) + a_{2}(-1,1,0)$ which implies that $[(1,0,1), (0,1,1), (-1,1,0)] = \im(T)$, but we need to check for [[Linear (In)dependence.|linear dependence]] to ensure it's a valid [[Theorems and Proofs for Basis and Dimension|basis]].
$$\begin{align*}
\begin{pmatrix}
1 & 0 & 1\\
0 & 1 & 1\\
-1 & 1 & 0
\end{pmatrix}
\implies
\begin{pmatrix}
1 & 0 & 1 \\
0 & 1 & 1\\
0 & 1 & 1 
\end{pmatrix}
\implies
\begin{pmatrix}
1 & 0 & 1 \\
0 & 1 & 1\\
0 & 0 & 0
\end{pmatrix}
\implies
[(1,0,1), (0,1,1)] &= \im(T)
\end{align*}$$
Because $\dim[\im(T)] \lt \dim(\mathbb{R}^{3}) \implies$ $T$ is not surjective. [[Rank of a Matrix|rank]] of the [[Augmented Matrix]] of $T$ must be equal the number of columns.
