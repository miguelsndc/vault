---
tags: trig
---
To find the length of the sides of a triangle if only the [[Angle|angles]] and the area are known *(or two angles, do $180 - A - B$ to find the third)*. Assume we are dealing with a non-[[Right Triangle]].

>[!tip] Definition:
>Let $c$ be a arbitrary unknown side of a triangle $\triangle{ABC}$ and $S$ be the area of $\triangle{ABC}$.
>
> $c^{2}= S\frac{2\sin{C}}{\sin{A}\sin{B}}$
> 
> *The square of a side $a$ is the area multiplied by two times the sine of the angle opposite to $a$ divided by the sines of the other angles*

# Derivation
Suppose the $\triangle{ABC}$ with Area = $S$.
![[Pasted image 20231221225454.png]]
Notice that $S = \frac{ah}{2}$ where $h$ is a segment from $A$ to $BC$.
See that $h = c\sin{B}$ *(or $b\sin{C}$, works either way)*, so:
$$\begin{align*}
S&= \frac{ac\sin{B}}{2}
\end{align*}$$
Notice we have two unknowns, $a$ and $c$, we can't solve it, we need to find a way to get the sides based of the area and the angles, we need to get rid of one side and solve for the other so, from the [[Law of Sines]]:
$$\begin{align*}
\frac{a}{\sin{A}}&= \frac{c}{\sin{C}}\\
a&= \frac{c\sin{A}}{\sin{C}}
\end{align*}$$
Substituting on $S$:
$$\begin{align*}
S&= \frac{c\sin{A}}{\sin{c}} \frac{c\sin{B}}{2}\\
S&= \frac{c^{2}\sin{A}\sin{B}}{2\sin{C}} 
\end{align*}$$
That's better, now solve for $c$:
$$\begin{align*}
\left(\frac{S}{c^{2}}\right)^{-1}&= \left(\frac{\sin{A}\sin{B}}{2\sin{C}}\right)^{-1} \\
\frac{c^{2}}{S}&= \frac{2\sin{C}}{\sin{A}\sin{B}} \\\\
c^{2}&= S\frac{2\sin{C}}{\sin{A}\sin{B}}
\end{align*}$$
> *The square of a side $a$ is the area multiplied two times the sine of the opposite angle of $a$ divided by the sines of the other angles*
