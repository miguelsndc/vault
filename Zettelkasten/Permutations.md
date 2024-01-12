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

## Proof
Let $S$ be a [[Sets|set]] such that $|S| = n$ 
There's $n$ ways to choose the first element. Since one element is taken, there is $n-1$ ways to pick the second element and so on. So it follows that there are $n-(r-1)=n-r+1$ ways to take the $r$-th element of $S$.

By the [[Product Rule]] there is:
$$\begin{align*}
P(n,r) =n(n-1)(n-2)\cdots(n-r+1)
\end{align*}$$
ways to take $r$ elements from $n$.
$P(n,0)=1$ because there's only one way to order zero elements, we can derive a general formula for permutations as such:

The "formula" for $r$-permutations above clearly describes a [[Factorials|factorial]], however, it is not **any** factorial, we want to multiply until we reach $n-r+1$, since factorials are just a product, we need to **divide by something** limit the multiplication, and we need to use $r$ on this somewhere, let's look at a simple example:
$$\begin{align*}
P(6,3) =6\cdot 5 \cdot 4 = 12\\
\end{align*}$$
The missing elements were exactly 




