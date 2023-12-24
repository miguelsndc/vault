---
tags: combinatorics
---
The generalized [[Pigeonhole Principle]] saysnthat if $N$ objects are placed into $k$ boxes, then there is at least one box containing $\lceil \frac{N}{k} \rceil$ objects.

# Proof 
Let us prove by [[Contradiction|contradiction]].
Suppose none of the boxes contain more than $\lceil \frac{N}{k} \rceil - 1$ objects, then, for $k$ boxes, the total number of objects is:
$$\begin{align*}
k(\left\lceil \frac{N}{k} \right\rceil -1)
\end{align*}$$
From the definition of [[Floor and Ceiling Functions|ceiling]] functions, we know that:
$$\begin{align*}
N &\le k\left(\left\lceil \frac{N}{k} \right\rceil -1\right)\lt k\left(\left(\frac{N}{k}+1\right)-1\right)\\
N &\le k\left(\left\lceil \frac{N}{k} \right\rceil -1\right)\lt k\left(\frac{N}{k}\right)\\
N &\le k\left(\left\lceil \frac{N}{k} \right\rceil -1\right)\lt N\\
N &\lt N \\
\bot
\end{align*}$$
From here we obtain $N \lt N$, a contradiction.