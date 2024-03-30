---
tags: spaces, vectors
aliases: gram-schmidt
---
Let $\beta = \{v_{1}, v_{2}, \cdots, v_{n}\}$ be a [[Theorems and Proofs for Basis and Dimension|basis]] for a [[Vector Space|vector space]] $V$ equipped with [[Inner Product|inner product]] $\innp{,}$. It's possible to obtain a [[Orthonormal Basis|orthonormal]] from $\beta$ using the *gram-schmidt orthogonalization process*. This works for any space.
The key idea is to choose a initial [[Vector|vector]] $v_{1}'$, then figure out a vector $v_{2}'$  from $v_{2}$ that is orthogonal to $v_{1}'$, then a $v_{3}'$ that is orthogonal to both $v_{1}'$ and $v_{2}'$, and so on until the $n$-th vector.
# Process
Let $v_{1}' = v_{1}$. We need to find, from $v_{2}$, a vector $v_{2}'$ that is [[Orthogonality|orthogonal]] to $v_{1}'$, that is, $\innp{v_{2}', v_{1}'}=0$. Let $v_{2}' = v_{2} - cv_{1}'$. where $c$ is chosen in a way that $\innp{v_{2}', v_{1}'}=0$. That is, $\innp{v_{2} - cv_{1}', v_{1}'}= 0$, which, from the [[Fourier Coefficients]], we know that $c=\frac{\innp{v_{2},v_{1}'}}{\innp{v_{1}', v_{1}'}}$.
Now we have:
$$\begin{align*}
v_{1}'&= v_{1}\\
v_{2}'&= v_{2}- \frac{\innp{v_{2},v_{1}'}}{\innp{v_{1}', v_{1}'}}v_{1}'
\end{align*}$$
Now we must find a vector $v_{3}'$ that is orthogonal **to both** $v_{1}'$ and $v_{2}'$. The reasoning is analogous. So $v_{3}'=v_{3}- \frac{\innp{v_{3},v_{1}'}}{\innp{v_{1}', v_{1}'}}v_{1} - \frac{\innp{v_{3},v_{2}'}}{\innp{v_{2}', v_{2}'}}v_{2}'$. After a finite number of steps we find a basis $\beta' = \{v_{1}', v_{2}', \cdots, v_{n}' \}$ given by:
$$\begin{align*}
v_{1}'&= v_{1}\\
v_{2}'&= v_{2}- \frac{\innp{v_{2},v_{1}'}}{\innp{v_{1}', v_{1}'}}v_{1}'\\
v_{3}'&= v_{3}- \frac{\innp{v_{3},v_{1}'}}{\innp{v_{1}', v_{1}'}}v_{1} - \frac{\innp{v_{3},v_{2}'}}{\innp{v_{2}', v_{2}'}}v_{2}'\\
\vdots\\
v_{n}'&= v_{n} - \frac{\innp{v_{n},v_{1}'}}{\innp{v_{1}', v_{1}'}}v_{1}'- \cdots-\frac{\innp{v_{n},v_{n-1}'}}{\innp{v_{n-1}', v_{n-1}'}}v_{n-1}'
\end{align*}$$
This is the process. Choose a pivot $v_{1}'$, then build new [[Orthogonality|orthogonal]] vectors by subtracting the current pivot from it's [[Orthogonal Projections]] of the already orthogonalized vectors. 3