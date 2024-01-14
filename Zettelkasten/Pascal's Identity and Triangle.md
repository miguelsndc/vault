---
tags: binomial-theorem, combinatorics
---
Let $n$ and $k$ be positive integers with $n \ge k$, then:
$$\begin{align*}
{n+1 \choose k} ={n \choose k-1 }+ {n \choose k}
\end{align*}$$
## Proof
We use a [[Combinatorial Proof]].  Suppose that $T$ is a [[Sets|set]] containing $n+1$ element. Let $a \in T$. and let $S= T- \{a\}$. Note that there are $n+1 \choose k$ [[Subsets]] of $T$ containing $k$ elements. However, a subset of $T$ with $k$ elements either contains $a$ together with $k-1$ elements of $S$ or contains $k$ elements of $S$ and does not contain $a$.
Because there are $n \choose k-1$ subsets of $k-1$ elements of $S$, there are $n \choose k-1$ [[Subsets]] of $k$ elements of $T$ *that contain* $a$. And there are $n \choose k$ subsets of $k$ elements of $T$ that do not contain $a$, because there are $n \choose k$ subsets of $k$ elements of $S$. Consequently:

