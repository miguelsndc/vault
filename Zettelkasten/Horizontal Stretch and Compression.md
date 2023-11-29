---
tags:
  - functions
  - graphs
  - transformations
date: 2023-10-06
"
page: 203
aliases:
  - horizontal stretch
  - horizontal shrink
  - shrink
  - stretch
---
Horizontally stretching or shrink stands for a transformation that makes the [[Graph of a Function|graph of]] a [[Functions|function]] **wider** or **narrower** without changing the $y$-values of it.
Suppose we have $y=f(x)$, Note:
- To horizontally **shrink** it, we can multiply $x$ by a constant $c$ where $c \gt 1$, because if:
$$\begin{align*}
f(x) &\rightarrow (x, f(x))\\
f(cx) &\rightarrow (cx, f(cx))\\
\end{align*}$$
This would give us the desired $y$-value, but the $x$-value is wrong, therefore to get the correct $x$, we must divide $cx$ by $c$ to get the original $x$. By doing this we are keeping the $y$-value while pushing it $\frac{1}{c}$ units closer the the $y$-axis, see:
$$\begin{align*}
f(x) &\rightarrow (x,f(x))\\
f(cx) &\rightarrow (cx,f(cx)) \;\text{We don't want this!}\\
f(cx) &\rightarrow \left(\frac{x}{c}, f(cx)\right) \; \text{Now x is preserved}
\end{align*}$$
Now for every ordered-pair, $y$ will keep the same value but will be closer the the $y-axis$, because the $x$ valued is **smaller**. Therefore it looks *shrinked*.
- To horizontally **stretch it**, we can multiply $x$ by a constant $c$ where $0 < c < 1$, because:
$$\begin{align*}
\text{Let } c &= \frac{1}{k} \;\text{because } 0 < \frac{1}{k}<1 \; \text {for}\; k<1
\\
f(x) &\rightarrow (x,f(x))\\
f(cx) &\rightarrow f\left(\frac{x}{k}\right)\rightarrow \left(x,f\left(\frac{x}{k}\right)\right)\; \text{We dont want this!!}\\
f(cx)&\rightarrow f\left(\frac{x}{k}\right)\rightarrow\left(xk,f\left(\frac{x}{k}\right)\right) \;x\;\text{ is preserved.}
\end{align*}$$
We are therefore stretching the graph $k$ units farther from the $y$-axis while keeping the $y$-values preserved, because $x$ is larger now the $y$ values are more separate, making it look *stretched*.
