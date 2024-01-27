---
tags: spaces, systems
---
Consider the [[Definition of a System of Linear Equations|system]]:
$$\begin{align*}
S_{1}=\Bigg\{ (x,y,z,w) \in \mathbb{R}^{3} \mid \begin{cases}
x-2y+3=0\\
2x+2y-z=0
\end{cases}\Bigg\}
\end{align*}$$
This system is in what is called a [[Implicit and Explicit forms of a Equations|implicit]] form, it doesn't explicitly state what [[Vector|vectors]] it is composed by, it just tells you a random property these vectors fulfill. 
However if conversion is necessary for some reason we can do as follows:
1. Find the [[Augmented Matrix]].
2. Put it in [[Echelon Form]].
3. Find and assign parameters to free variables, if there's any
4. Put it in the fancy notation and we are done.
See, the augmented matrix of $S_{1}$ is:
$$\begin{align*}
\begin{pmatrix}1 & -2 & 3\\
2 & 2 & -1\\
\end{pmatrix}
\end{align*}$$
In [[Echelon Form]]:
$$\begin{align*}
\begin{pmatrix}
1  & 0 & \frac{2}{3}\\
0 & 1 & -\frac{7}{6}
\end{pmatrix}
\end{align*}$$
The third column has no [[Pivot|pivots]], therefore we can assign a free variable to it. Let's call each column from left to right, $x,y$ and $z$ respectively, so:
$$\begin{align*}
\begin{cases}
x+ \frac{2}{3}z &= 0\\
y- \frac{7}{6}z&= 0\\
\end{cases}
\end{align*}$$
$$\begin{align*}
\begin{cases}
x+ \frac{2}{3}z &= 0\\
y- \frac{7}{6}z&= 0\\
\end{cases}
\end{align*}$$
Let's assign $z$ a paremeter $t \in \mathbb{R}$ and isolate the variables from the coefficients:
$$\begin{align*}
\begin{cases}
x= -\frac{2}{3}t\\
y= \frac{7}{6}t\\
z=t
\end{cases}
\end{align*}$$
We actually have a [[vector]] $v$ being multipled by a constant $t$, so the parametric form of this system is all the [[Linear Combinations]] of $v$:
$$\begin{align*}
S_{1}=\{(x,y,z) \in \mathbb{R}^{3}\mid (x,y,z) &= t(-\frac{2}{3}, \frac{7}{6}, 1\}
\end{align*}$$
There's our fancy notation.
___
To convert it back to the implicit form we can form a matrix where each column will be a vector described in the explicit form, and add one more column of variables.
Let $S_{3} = \{  (x,y,z,w) \in \mathbb{R}^{4} \mid (x,y,z,w) = w(-2,0,0,1) + z(0,1,1,0) + t(-2,-3,5,1)  \}$ 
So our [[Matrix Definition|matrix]] is:
$$\begin{align*}
\begin{pmatrix}
-2 & 0 & -2 & \mid  x\\
0 & 1 & -3 & \mid y\\
0 & 1 & 5 & \mid z\\
1 & 0 & 1 & \mid w
\end{pmatrix}
\end{align*}$$
We can quickly find it, such as:
$$\begin{align*}
\begin{pmatrix}
0 & 0 & 0 & \mid  x+2w\\
0 & 1 & -3 & \mid y\\
0 & 1 & 5 & \mid z\\
1 & 0 & 1 & \mid w
\end{pmatrix}
\end{align*}$$
So our explicit form is $S_{3}=\{(x,y,z,w) \in \mathbb{R}^{4} \mid x+2w=0\}$.