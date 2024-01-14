---
tags: binomial-theorem, combinatorics
---
Let $n$ and $k$ be positive integers with $n \ge k$, then:
$$\begin{align*}
{n+1 \choose k} ={n \choose k-1 }+ {n \choose k}
\end{align*}$$
## Proof
Let $S$ be a set with $n+1$ elements, and consider some fixed $x \in S$. There are $n+1 \choose r$ r-[[Subsets]] of $S$, By counting them according to whether they contain or not $x$: There are $n \choose r$ [[Subsets]] of $r$-elements that do not contain $x$, (counted by choosing $r$ elements from the remaining $n$ elements of $S \textbackslash \{x\}$) and there are $n \choose r-1$ $r$-[[Sets]] containing $x$, since $x$ is already contained, there's $r-1$ left to choose from $n+1 -1 = n$ elements left. Consequently

$$\begin{align*}
{n+1 \choose k} ={n \choose k-1 }+ {n \choose k}
\end{align*}$$