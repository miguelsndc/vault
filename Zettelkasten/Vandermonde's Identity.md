---
tags: binomial-theorem, combinatorics,
aliases: vandermonde
---
Let $m$, $n$, $r$ be nonnegative integers with $r$ not exceeding either $m$ or $n$, then:
$$\begin{align*}
{m+n\choose r}=\sum\limits_{k=0}^{n}{m\choose r-k}{n\choose k}
\end{align*}$$
## Proof
Suppose there are $m$ elements in one [[Sets|set]] and $n$ elements in a second set. The number of ways to choose $r$ elements from the [[Union]] of those sets is ${m+n \choose k}$, Suppose we choose $k$ elements from $n$, with $0 \le k \le r$, then, we need to choose more $r-k$ elements in $m$, and the number of ways to do so is ${m \choose r-k}{n \choose k}$, by the [[Product Rule]].
This proves vandermonde's identity.