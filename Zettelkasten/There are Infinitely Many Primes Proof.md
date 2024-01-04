---
tags: number-theory, proofs
---
We use prove by [[Contradiction|contradiction]], assume there's **finitely** many primes, $p_{1},p_{2},\cdots, p_{n}$. Let:
$$\begin{align*}
Q &= p_{1},p_{2},\cdots, p_{n} + 1
\end{align*}$$
By The [[Fundamental Theorem of Arithmetic]], $Q$ is [[Prime Numbers|prime]] or can it can be written as a product of two or more primes. However, none of the primes $p_{j}$ divides $Q$ for it, if $p_{j} \mid Q$ then $p_{j}$ divides $Q - p_{1},p_{2},\cdots, p_{n} = 1$, Hence, there is a prime on the list $p_{1},p_{2},\cdots, p_{n}$. This prime is either $Q$ or a prime factor of $Q$. 
Which forms a contradiciton.