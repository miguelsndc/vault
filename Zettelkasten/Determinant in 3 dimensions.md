---
tags: vectors
---
Let $a, b$ and $c$ be [[Vector|vectors]] in $\R^{3}$, the **determinant** $\det(a,b,c)$ equals the **volume** of the parallelepiped spanned by $a, b$ and $c$.
## Why is that ?
We know about areas of parallelograms using [[Cross Product|cross]] products, which is the area of the base, since the volume of a parallelepiped is $\f{area}(base) \cdot height$, we need to figure out the height.
![[DET3]]
The area of the base is $\norm{b \times c}$, and the height is the [[Components of vector along some direction|component]] of $a$ along the direction $\hat{u}$  which is normal to the plane spanned by $c$ and $d$, so $a \cdot \hat{u}$ will do the trick. Now we must find $\hat{u}$, our area formula is looking like this: $\f{Vol} = \norm{b \times c}(a \cdot \hat{n})$.

The cross product $b \times c$ will not only give us the area of the base, but a vector perpendicular to both $b$ and $c$, so we only need to normalize it: $\hat{n} = \frac{b \times c}{\norm{b \times c}}$.
$$\begin{align*}
\f{Vol}&= \norm{b \times c} (a \cdot \hat{n})\\
&= \norm {b \times c} (a \cdot \frac{b \times c}{\norm{b \times c}})\\
&= a \cdot (b \times c)\\
&= a \cdot \begin{matrix}
\hat{i} & \hat{j} & \hat{k}\\
b_{1} & b_{2} & b_{3}\\
c_{1} & c_{2} & c_{3}
\end{matrix}\\
&= a \cdot (
\hat{i}\det\begin{pmatrix}b_{2} & b_{3}\\ c_{2} & c_{3}\end{pmatrix}
- \hat{i}\det\begin{pmatrix}b_{1} &b_{3} \\ c_{1} & c_{3}\end{pmatrix}
  + \hat{k} \det\begin{pmatrix} b_{1} & b_{2}\\ c_{1} & c_{2}  \end{pmatrix}
)  \\
&= a \cdot (\hat{i}(b_{2}c_{3}-b_{3}c_{2})-\hat{j}(b_{1}c_{3}+b_{3}c_{1})+ \hat{k}(b_{1}c_{2}- b_{2}c_{1}))\\
&= a \cdot \innp{b_{2}c_{3}-b_{3}c_{2},b_{3}c_{1}-b_{1}c_{3},b_{1}c_{2}-b_{2}c_{1}}\\
&= \innp{a_{1},a_{2},a_{3}} \cdot \innp{b_{2}c_{3}-b_{3}c_{2},b_{3}c_{1}-b_{1}c_{3},b_{1}c_{2}-b_{2}c_{1}}\\
&= a_{1}b_{2}c_{3}-a_{1}b_{3}c_{2}+a_{2}b_{3}c_{1}-a_{2}b_{1}c_{3}+a_{3}b_{1}c_{2}-a_{3}b_{2}c_{1}\\
&= \det\begin{pmatrix}
a_{1} & a_{2} & a_{3} \\
b_{1} & b_{2} & b_{3}\\
c_{1} & c_{2} & c_{3}
\end{pmatrix}
\end{align*}$$
Thus we have shown that $\det(a,b,c)$ is the volume of the parallelepiped created by them.c


