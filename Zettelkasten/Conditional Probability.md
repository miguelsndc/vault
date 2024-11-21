---
tags: probability, statistics
aliases: conditional
---
Sometimes the phenomena we're dealing with can be broke into parts, what happened in one part can influence the [[Probability|probabilities]] of the next parts. Thus we gain information and can recalculate the probabilities of interest, those are called **conditional probabilities**. Testing

Let $A$ and $B$ be two [[Event|events]] of $\Omega$, then the *conditional probability* of **$A$ given that $B$ happened**, is denoted $P(A \mid B)$, where:
$$\begin{align*}
P(A \mid B) &= \frac{P(A \cap B)}{P(B)}
\end{align*}$$
Without much effort we can see that $P(A \cap B) = p(A \mid B) P(B)$.