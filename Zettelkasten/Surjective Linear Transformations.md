---
tags: linear-transformations
---
In case of [[Functions]] in general, [[Strategies to Prove Surjectivity|surjectivity]] is defined as: Let $f: A \rightarrow B$, then if is surjective if and only if $\forall b \in B \;\; \exists a \in A \mid f(a) = b$. When talking about [[Linear Transformations]], surjectivity is defined through the [[Image of a linear transformation|image]]: 
Let $T:V \rightarrow W$ be a linear transformation, $T$ is surjective [[If and Only if|if and only if]], $\im(T) =W$, since $\im(T) \subset W$, if the [[Theorems and Proofs for Basis and Dimension|dimension]] of $W$ and $\im(T)$ are the same then $\im(T) = W$. ($\dim[\im(T)] = \dim(W)$.
So let $\{v_{1},v_{2},\cdots, v_{n}\}$ be a [[Theorems and Proofs for Basis and Dimension|basis]] of $\im(T)$, (since the image is a [[Linear Subspaces|subspace]].) if $n = \dim(W)$, then ${v_{1}, v_{2},\cdots, v_{n}}$ is also a [[Theorems and Proofs for Basis and Dimension|basis]] for $W$ and hence $\im(T) = W$ since the [[Span|span]] of both cover the same [[Linear Subspaces|subspace]].
## How to find it
We want to know whether the [[Theorems and Proofs for Basis and Dimension|dimension]] of both $\im(T)$ and $W$ on $T:V \rightarrow W$, are the same, so, when defining a [[Linear Transformations|linear transformation]] we usually know which space it's being mapped to which space, therefore knowing it's dimension. Therefore, simply finding a [[Theorems and Proofs for Basis and Dimension|basis]] for $\im(T)$ will do the job, and if the number of elements in the basis of $\im(T)$ is equal to the dimension of $W$ then they are the same hence $T$ is [[Surjective Functions|surjective]].
$\rm{Example}:$ 
Let $$
