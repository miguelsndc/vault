---
tags: vector
aliases: determinant
---
![[triangle]]
The area of the above triangle is $\frac{1}{2}\norm{b}\norm{a}\sin{\theta}$ (*half base * height*), but we don't know sines! But we're pretty good at cosines, using [[Dot Product]]'s, we could solve for $\sin{\theta}$ then substitute into $\sin^{2}{\theta} + \cos^{2}{\theta} = 1$, but that's a lot of work. instead we can use determinants:
![[det]]
 If we rotate $a$ $90$ degrees counterclock-wise we get a new vector $a'$ and a new angle $\theta'$, so $\theta'=\frac{\pi}{2}-\theta \implies \cos(\theta')=\sin{\theta}$, the formula becomes $\norm{a'}\norm{b}\cos{\theta'}= a' \cdot b$. Much simpler. To rotate $a$ $\frac{\pi}{2}$ counterclock-wise we need some sort of reflection, we can accomplish this algebraically:$$\begin{align*}
a'\cdot a&= 0\\
\innp{a'_{1},a'_{2}}\cdot \innp{a_{1},a_{2}}=0\\
a'_{1}a_{1}+a'_{2}a_{2}=0\\
a'_{1}a_{1}=-a'_{2}a_{2}\\
a'_{1}a_{1}=-a_{2}a'_{2}
\end{align*}$$
We can see that $a'_{1}=-a_{2}$ and $a'_{2}=a_{1}$ is the solution, so $a'= \innp{-a_{2},a_{1}}$. *(Actually multiplying $a$ by $\begin{pmatrix}0 & -1\\1 & 0\end{pmatrix}$*. So putting everything in the formula:
$$\begin{align*}
a'\cdot b&= \innp{-a_{2},a_{1}}\cdot\innp{b_{1},b_{2}}\\
&= a'_{1}b_{2}-a'_{2}b_{1}\\
&= \det\begin{pmatrix}a_{1} & a_{2}\\b_{1} & b_2\end{pmatrix}\\
&= \det{(a,b)}
\end{align*}$$
Which is the determinant of [[Vector|vectors]] $a$ and $b$. The determinant corresponds to the area of the parallelogram formed by $a$ and $b$, quick disclaimer: Areas are positive, however if $a'$ and $b$ are pointing in different directions the cosine becomes negative, so a better definition is: $\det(a,b)= |$ Area of paralellogram formed by $a$ and $b$ $|$ $= \norm{a}\norm{b}\sin{\theta}$.