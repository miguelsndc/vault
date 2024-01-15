---
tags: combinatorics
---
With [[Permutations]] we count the amount of $r$ subsets of a set with $n$ elements, with order in mind, meaning $\{a,b,c\} \ne \{b,a,c\}$. However, in a situation where order is *irrelevant*, permutations overcount.
Let $P(n,r) = \frac{n!}{(n-r)!}$ 
$P$ counts the number of $r$-permutations of $n$ elements. Observe that every $r$ set with $0 \le |r| \le |n|$ has exactly $r!$ permutations of it's own elements. We know $\frac{r!}{r!}= 1$, By dividing the $P$ by the number of permutations of $r$ we are considering every $r$ subset only once regardless of the orders. So the formula becomes:
$$\begin{align*}
P'=\frac{n!}{r!(n-r)!}
\end{align*}$$
This $P'$ is called a **combination**. It counts the number of ways to **choose $r$ elements from $n$** elements. *(Note permutations count the number of ways to order $r$ elements in $n$)*. 