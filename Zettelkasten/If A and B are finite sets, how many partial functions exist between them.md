---
tags: proofs
---

> [!question]  Prove
> If $A$ and $B$ are finite [[Sets|sets]], how many [[Partial Function|partial functions]] exists between them?

A Partial function $f: A \rightarrow B$ maps some subset $X$ of $A$ to $B$ where $(0 \le |X| \le |B|)$, Let $|X| = k$, There are $|B|^{k}$ mappings possible from $X$ to $B$. And also there's $\begin{pmatrix}|A| \\ k\end{pmatrix}$ ways to choose a subset $X$ with $k$ elements from $A$, so the total number of partial functions is the summation:
$$\begin{align*}
\sum_{k=0}^{|A|}\begin{pmatrix}|A|\\
k\end{pmatrix}|B|^{k}&= (1+|B|)^{|A|}
\end{align*}$$
So from a set with $n$ elements from a set with $x$ elements there are $(1+x)^n$ partial functions.