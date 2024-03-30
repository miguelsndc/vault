---
tags: vector
---
From the [[Schwarz Inequality]] it's possible to define and generalize the notion of [[Angle|angle]] between two [[Vector|vectors]]. Let $V$ be a [[Vector Space|vector space]] with [[Inner Product]] $\innp{,}$, also let $v,w \in V$, then:
$$\begin{align*}
\abs{\innp{v,w}} &\le \norm{v} \cdot \norm {w}\\
\frac{\abs{\innp{v,w}}}{\norm{v} \cdot \norm{w}} &\le 1
\end{align*}$$
Which implies that exists some angle $\theta$ between $0$ and $\pi$ [[Degrees and Radians|radians]] such that $\cos{\theta} =\frac{\abs{\innp{v,w}}}{\norm{v} \cdot \norm{w}}$.
One can find such angles with the inverse cosine function. 

> Notice this is for any $n$-dimensional space.