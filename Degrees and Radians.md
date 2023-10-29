---
tags:
  - "#trigonometry"
date: 2023-10-29
link: https://brownmath.com/twt/intro.htm
aliases:
  - radians
  - degrees
---
Degrees and Radians are different ways to measure angles. In radians we use a ratio of $\pi$, and with degrees we simply use numbers.

The most famous use case of these measures relies on measuring the [[Unit Circle|unit circle]]. By convention, a full turn in a circle is $360\degree$ or $2\pi$. So it follows that half a turn is $180\degree$ and $\pi$, respectively.
#### Converting one from another
To convert from degrees to radians and vice-versa we remember our ratio $180\degree = \pi$. 
Let's derive the conversion of $\frac{3\pi}{4}$ to degrees, you probably guessed that we need to multiply the top part by $180$, and that's correct.
$$\begin{align*}
\frac{3\pi}{4}\cdot 180&= \frac{540\pi}{4}
\end{align*}$$
But we also need to drop the $\pi$ here, so:
$$\begin{align*}
\frac{540\pi}{4} \cdot \frac{1}{\pi}&= \frac{540}{4}=135\degree
\end{align*}$$
Notice that all we did was multiply by $180/\pi$. which is, algebraically the same as multiplying by one since $\pi = 180$ then $\frac{180}{180}=1$. We **did not change** the value of angle.

Same process goes for degrees to radians, Converting $270\degree$ to radians. Think of $270\degree$ as a already converted radian, so $270\degree$ is already multiplied by $180$ and divided by $\pi$, so we need to do the opposite:
$$\begin{align*}
x\left(\frac{180}{\pi}\right)&= 270\\
\frac{180x}{\pi} &= 270\\
180x &= 270\pi\\
x &= \frac{1}{2}\pi\\
x&= \frac{\pi}{2}
\end{align*}$$
So paying attention, what we really did was multiply by $\frac{\pi}{180}$.

Notice the pattern:
- Convert from degrees to radians, drop the $180\degree$ and multiply by $\pi$ 
- Convert from radians to degrees, drop $\pi$ and multiply by $180\degree$.