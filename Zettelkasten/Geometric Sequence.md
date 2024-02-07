---
tags: 
---
A Geometric sequence is a sum of numbers where each term after the first is found by multiplying the previous one by a fixed, non-zero number called the **common ratio**, For example, the sequence $2,6,18,54\cdots$ is has a common ratio of $3$.

Examples of geometric sequences are powers $r^{k}$, of a fixed non-zero number $r$, like $2^{k}$, The general form is:
$$\begin{align*}
a,ar,ar^2,ar^3,\cdots,ar^{n-1},ar^{n}
\end{align*}$$
Where $r\ne0$ is the common ratio and $a$ is known as a scale factor.
___
We can find any term of such sequences by multiplying the scale factor $a$ by the **ratio** raised to a power $n-1$, where $n$ is the power we want, since $ar^{0}$ is the first term.
$$\begin{align*}
10,30,90,270,\cdots
\end{align*}$$
The ratio os $3$ and the scale factor is $10$, we can find the $4$th term as follows:
$$\begin{align*}
10\cdot3^{4-1}=10\cdot3^{3}=270
\end{align*}$$
Which is indeed the fourth term.
___
We can also find the total sum of terms of a geometric sequence as such:
$$\begin{align*}
S_{n}=a_{1}\left(\frac{1-r^{n}}{1-r}\right)
\end{align*}$$
Where:
- $a_{1}$ is the first term of the sequence, or the **scale factor**.
- $r$ is the common ratio.
- $n$ is the total number of terms in the sequence
Notice that if a sequence starts from $ar^{0}$ and goes through $ar^{n}$, it has $n+1$ terms, since the zero is present.
The sequence $10,30,90,270$, has a sum of:
$$\begin{align*}
S_{n}&= 10\left(\frac{1 - 3^{4}}{1-3}\right)\\
&= 10\left(\frac{1-81}{-2}\right)\\
&= \frac{10-810}{-2}\\
&= \frac{-800}{-2}=400
\end{align*}$$
And indeed $10+30990+270 = 400$.
____
We can find the ratio by dividing the $n$th term with the $n-1$ term, and keep dividing until we are certain of the ratio. Geometric sequences usually involve powers, and it's quite easy to see them and notice the ratios.
