---
tags: derivatives
aliases: derivative, derivatives
---
First we introduce a [[Functions in Discrete Math|function]] $f$ and a open interval $(a,b)$, we let $x$ and $x+h$ lie in this interval, we wish to calculate the rate of change from $x$ from $x+h$, so we introduce the [[Difference Quotient]], See:
$$\begin{align*}
\lim_{h\to 0} \frac{f(x+h) - f(x)}{h}
\end{align*}$$
Now we let $h$ approach zero and see what happens to this quotient, if we approach a **definite** value as this limit approaches $0$ *(from the positives **and** from the negatives, so, this limit exists)*, we say the this limit is the **derivate** of $f$ at $x$ and is denoted as $f'(x)$. So:
$$\begin{align*}
f'(x)=\lim_{h\to 0}\frac{f(x+h)-f(x)}{h}
\end{align*}$$
We call $f'(x)$ the *first derivative* of $f$, we can calculate it's first derivative, $f''(x)$, the first derivate of $f'$ and the *second derivative* of $f$. We can calculate the $n$th derivate and denote it as $f^{(n)}$ and we call $f^{(n)}$ the first derivative of $f^{(n-1)}$. We the convention that $f^{(0)}=f$, that is, the zeroth derivative is the function itself.