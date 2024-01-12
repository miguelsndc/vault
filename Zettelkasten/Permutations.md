---
tags: combinatorics
---
Permutations are a counting principle that count the number of ways to arrange $n$ objects.

> [!tip] Definition
> A permutation of a [[Sets|set]] of distinct objects is an ordered arrangement of these objects.

Permutations inspired and are defined in terms of [[Factorials]].
Ex: *The number of ways to arrange $4$ people in a line is $4!$=$24$*.
___
We are also interested in a ordered arrangement of *some* elements. A ordered arrangement of $r$ elements from a set of $n$ is called a *$r$-permutation*.
Let $P(n,r)$ denote the number of $r$-permutations from a [[Sets|set]] of $n$ elements.

"Let $S = \{a,b,c\}$, the $2$-permutations of $S$ are: $ab,ac,ba,bc,ca,cb$. There is always **six $2$-permutations from a set of $3$ elements**, since there's $3$ ways to take the first and $2$ ways to take the second, by the [[Product Rule]]: $3\cdot2=6$ ways, or $P(3,2)=6$"

>[!tip] Theorem
>If $n \in \mathbb{Z}^{+}$$ and $r\in \mathbb{Z}^{+} \mid 1 \le r \le n$, then:
>$P(n,r)=n(n-1)(n-2)\cdots(n-r+1)$ $r$-permutations of a set with $n$ elements.
>
