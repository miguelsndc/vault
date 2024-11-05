---
tags: ml, ds, probability
aliases: continuity
---
The theorem of the [[Continuity of A Function|continuity]] of [[Probability|probabilities]] say that if $A_{n}\rightarrow A$, then $\P(A_{n})\rightarrow \P(A)$ as $n \rightarrow \infty$.

Suppose that $A$ is **monotone increasing**, that is $A_{1} \subset A_{2} \subset \cdots$, Let $A = \lim_{n\rightarrow \infty} A_{n} = \bigcup_{i=1}^{\infty}A_{i}$. Define $B_{1} = A_{1}$, $B_{2} = \{\omega \in \Omega \mid \omega \in A_{2}, \omega \notin A_{1}\}$, $B_{3} = \{\omega \in \Omega \mid \omega \in A_{3}, \omega \notin A_{2}, \omega \notin A_{1}\}, \cdots$. Those [[Subsets]] are [[Disjoint Set|disjoint]] by definition. $A_{n}=\bigcup_{i=1}^{n}A_{i}= \bigcup_{i=1}^{n}B_{i}$, also $\bigcup_{i=1}^{\infty}A_{i} = \bigcup_{i=1}^{\infty}B_{i}$. From the rules of probability:
$$\begin{align*}
\P(A_{n})=\P\left(\bigcup_{i=1}^{n}B_{i}\right) &= \sum\limits_{i=1}^{n}\P(B_{i})
\end{align*}$$
So, from the same rules again:
$$\begin{align*}
\lim_{n\rightarrow \infty}\P(A_{n})&= \lim_{n\rightarrow\infty}\sum\limits_{i=1}^{n}\P(B_{i})=\sum\limits_{i=1}^{\infty}\P(B_{i})=\P(A)
\end{align*}$$
This is stating that the probability of monotonically increasing [[Event|events]] tend to the probability of the entire [[Sample Space]], this establishes a connection between the events and their probabilities, when the events converge, their probabilities also converse, small changes in events cause small changes in their probabilities, so **probabilities are pretty much continuous functions of their events**.
