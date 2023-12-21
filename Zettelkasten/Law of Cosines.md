---
tags: trig
---
[[Law of Sines]] is good to realte sides and [[Angle|angles]], but with three sides and no angles, law of sines can't be applied since it depends on the relation of the angles, that's when the **Law of Cosines** comes in:

>[!tip] Law of Cosines
>Identity that relates sides to angles in a triangle, has two main forms:
>$1$*st* form: $\cos{C}= \frac{a^{2}+b^{2}-c^{2}}{2ab}$ 
>$2$*nd* form: $c^{2} = a^{2}+b^{2}-2ab\cos{C}$

The first form is used to find the angles of a triangle when only sides are known: *the cosine of an angle $\theta$ is the sum of the squares of the two adjacent sides minus the square of the opposite side, divided by $2$ times the adjacent sides*. Notice we can find the angle by $\arccos{\theta}$.

The second form allow us to find the length of a side opposite two an angle $C$ between two known sides. *the square of a side $c$ is the sum of the squares of the other sides minus 2 times cosine of the angle opposite to $C$ and the other sides*.
It's a general form of [[Pythagorean Theorem]], but with the $2ab\cos{C}$ correction factor, to it works not only for [[Right Triangle|right triangles]].
# Proof
See the triangle $\triangle{ABC}$: 

![[Pasted image 20231221170646.png]]

> *Disclaimer: in the [[Law of Sines]] proof page, we found the cosines of the angles and didn't really use them, now we will.*

- We know:
$$\begin{align*}
\cos{A}&= \frac{AD}{c}\implies AD=c\cos{A}\\
\cos{C}&= \frac{CD}{a}\implies CD=a\cos{C}
\end{align*}$$
We can find a relation between these two by the [[Pythagorean Theorem]] and the segment $BD$:
$$\begin{align*}
(CD)^{2}+(BD)^{2}&= a^{2}\\
(AD)^{2}+(BD)^{2}&= c^{2}\\
(BD)^{2}&=a^{2}-(CD)^{2}\\
(BD)^{2}&= c^{2}- (AD)^{2} 
\end{align*}$$
Since $(BD)^{2}$ is equal to two expressions, we can equate them, but notice that: $CD+AD = b$, so $CD = b - AD$ *(or vice-versa)*.
$$\begin{align*}
a^{2}-(CD)^{2}&= c^{2}-(AD)^{2}\\
a^{2}-(b-c\cos{A})^{2}&= c^{2}-(c\cos{A})^{2}\\
a^{2}-(b^{2} - 2bc\cos{A} + c^{2}\cos^{2}{A})&= c^{2}-c^{2}\cos^{2}{A}\\
a^{2}-b^{2}+2bc\cos{A}-c^{2}\cos^{2}{A}&= c^{2}-c^{2}\cos^{2}{A}\\
a^{2}-b^{2}+2bc\cos{A}&= c^{2}\\
2bc\cos{A}&= b^{2}+c^{2}-a^{2}\\
\cos{A}&= \frac{b^{2}+c^{2}-a^{2}}{2b}
\end{align*}$$
Which shows the **first form**, now the se