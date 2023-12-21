---
tags: trig
---
The law of sines relates the sides of a triangle and the sines of the [[Angle|angles]] opposite to them:

>[!tip] Definition
>In **any type of triangle**, given the the angles $A, B$ and $C$ and the sides $a, b$ and $c$, where $a$ is opposite to $A$, $b$ is opposite to $B$ and $c$ is opposite to $C$, the law of sines states that:
>
>$$
\begin{align*}
\frac{a}{\sin{A}}=\frac{b}{\sin{B}}=\frac{c}{\sin{C}}
\end{align*}
>$$

Forming a relation of proportin between the sides and the sine of their opposite angles.
## This is Useful when:
- We know two angles and any side;
- Two angles and the area;
- *(Sometimes)* two sides and one angle;
# Proof
Divide in two cases: **Acute** and **Obtuse** Triangles:
- Acute triangles case:
![[Pasted image 20231221125511.png]]
In the figure we drawn a straight line from $A$ to the opposite side. From here we can see the following:
$$\begin{align*}
\sin{C} &= \frac{h}{b}\\
\sin{B} &= \frac{h}{c}\\
\therefore h&= b\sin{C}\\
h&= c\sin{B} 
\end{align*}$$
Since we have two values for $h$ we can equate them:
$$\begin{align*}
b\sin{C}&= c\sin{B}\\
\frac{b\sin{C}}{(\sin{C})(\sin{B})}&= \frac{c\sin{B}}{(\sin{C})(\sin{B})}\\
&\implies \frac{b}{\sin{B}}=\frac{c}{\sin{C}}
\end{align*}$$
Repeating the above but with altitude drawn from point $B$

![[Pasted image 20231221130131.png]]

