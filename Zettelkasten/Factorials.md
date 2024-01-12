---
tags: combinatorics
aliases: factorial
---
Factorials are a mathematical expression highly useful in combinatorics to describe the number of permutations of $n$ objects.
Let $n = 50$, let there be no reposition of objects.
There's $50$ ways to choose the first object, and, since the first object is taken, we have $49$ ways to take the next one, and it follows until it reaches $1$. by the [[Product Rule]], we have $50\cdot49\cdot \;\cdots\; \cdot 1$ ways to choose these objects. however, it's extremely unconvinient to write down all this, and mathematicians invented a notation:
$$\begin{align*}
50!=50\cdot49\cdot \;\cdots\; \cdot 2 \cdot 1
\end{align*}$$
For $n$ objects factorials are: 
$$\begin{align*}
n!=n(n-1)(n-2)\cdots(n-n)!
\end{align*}$$
Note that $0!=1$ because there is exactly one way to order zero elements.
