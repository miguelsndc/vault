---
tags: ml, ds, probability
aliases: continuity
---
The theorem of the [[Continuity of A Function|continuity]] of [[Probability|probabilities]] say that if $A_{n}\rightarrow A$, then $\P(A_{n})\rightarrow \P(A)$ as $n \rightarrow \infty$.

Suppose that $A$ is **monotone increasing**, that is $A_{1} \subset A_{2} \subset \cdots$, Let $A = \lim_{n\rightarrow \infty} A_{n} = \bigcup_{i=1}^{\infty}A_{i}$. Define $B_{1} = A_{1}$, $B_{2} = \{\omega \in \Omega \mid \omega \in A_{2}, \omega \notin A_{1}\}$, $B_{3} = \{\omega \in \Omega \mid \omega \in A_{3}, \omega \notin A_{2}, \omega \notin A_{1}\}, \cdots$. Those [[Subsets]] are [[Disjoint Set|disjoint]] by definition.  
