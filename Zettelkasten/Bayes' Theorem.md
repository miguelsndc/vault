---
tags: probability
---
First, let's define a **partition** of a [[Sample Space]]. The [[Event|events]] $C_{1},C_{2}, \cdots, C_{k}$ form a partition of $\Omega$, if, they **don't intersect** and **their union is the sample space**, that means:
$$\begin{align*}
C_{i} \cap C_{j}&= \emptyset\;,i\ne j;\\
\bigcup\limits_{i=1}^{k}C_{i}&= \Omega,
\end{align*}$$
So, the [[Probability|probability]] $P$ of some event $A$, is equal to the sum of the intersections of $A$ with each of the members of the partition: $P(A) = P(A\cap C_{1}) + P(A \cap C_{2}) + \cdots + P(A \cap C_{k})$.
___
Suppose the events $C_{1},C_{2}, \cdots, C_{k}$ form a partition of $\Omega$ with known probabilites. Suppose also that for some event $A$, the probabilities $P(A \mid C_{i}), \; i=1,2,\cdots,k$ are known, so, for any $j$:
$$\begin{align*}
P(C_{j}\mid A)&=\frac{P(A \mid C_{j})P(C_{j})}{P(A)} = \frac{P(A \mid C_{j})P(C_{j})}{\sum\limits_{i=1}^{k}P(A\mid C_{j})P(C_{j})}
\end{align*}$$
## Proof
From the definition of [[Conditional Probability]] we know that:
$$\begin{align*}
P(C_{j}\mid A)&= \frac{P(C_{j}\cap A)}{P(A)}
\end{align*}$$
We can rewrite the numerator as: $P(C_{j} \cap A) = P(A \cap C_{j})=P(A \mid C_{j})P(A)$.
Also note that $P(A) = \sum\limits_{i=1}^{k}P(A \cap C_{j})= \sum\limits_{i=1}^{k}P(A \mid C_{j})P(A)$..
