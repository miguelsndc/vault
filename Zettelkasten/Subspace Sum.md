---
tags: spaces
---
[[Subspace Intersection]] works by the regular [[Intersection]] definition of [[Sets]], however, joining two [[Linear Subspaces|subspaces]] requires more work that just a [[Union]]. 
Let $V$ be a [[Vector Space]] and $S_{1},S_{2}\subset V$ with $S_{1}$ and $S_2$ being subspaces.
Regular union as $S_{1}\cup S_{2}$ might not always be closed under addition, as example, consider two perpendicular lines that intersect each other at the origin. Using regular union will break addition closure if we pick two vectors from different lines and add them. However the union is indeed closed under [[Scalar]] multiplication. Therefore some pretty smart people defined the subspace "union" by filling the gaps of addition, and there's this definion for the sum of two subspaces. *sum, not union tho*.
$$\begin{align*}
S_{1}+S_{2}=\{v \in V \mid v=v_{1}+v_{2} \text{ where } v_{1} \in S_{1} \text{ and } v_{2}\in S_{2} \}
\end{align*}$$
There's a couple things about this notation:
1. $S_{1}\cup S_{2}\subset S_{1}+S_{2}$
The union is contained in the sum, if we take only the **zero** vector from one set and sum with every vector from the other set, we get the other set as result. doing it both ways results in the union.
Proof:
$$\begin{align*}
v&= v_{1}+v_{2}, \;\;\;v_{1}\in S_{1},v_{2}\in S_{2}\\
v&= v_{1}+\vec{0}=v_{1}\implies S_{1}\subset S_{1}+S_{2}\\
v&= \vec{0}+v_{2}=v_{2}\implies S_{2}\subset S_{1}+S_{2}\\
&\therefore S_{1}\cup S_{2}\subset S_{1}+S_{2}
\end{align*}$$
2. $S$