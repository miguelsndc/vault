---
tags: vector, functions
aliases: vector valued functions, vector function
---
A [[Vector]] valued [[Functions|function]] is a one-variable function $f:A \rightarrow \R^{n}$ $A \subset \R$ that maps every $t \in A$ in it's [[Domain]] to [[Vector|vectors]] in $\R^{n}$, every [[Components of vector along some direction|component]] of the vector is itself a function of $t$. specifically in $\R^{3}$, a vector function $\vec{r}(t)$ is given by:
$$\begin{align*}
\vec{r(t)}&= \hat{i}\,x(t) + \hat{j}\,y(t)+\hat{k}\,z(t)\\
&= \innp{x(t),y(t),z(t)}
\end{align*}$$
These being vectors that point from the origin to $r(t)$.
___
## Operations
Vector valued functions support both [[Vector|vector]] operations and [[Functions|function]] operations.

Let $F, G:A \rightarrow\R^{n}$ be two vector-valued functions, let $f:A\rightarrow \R$ be a [[Real Numbers|real]] function and $k \in \R$ a constant, the following operations are defined:

- $F+G:A\rightarrow \R^{n}$ is given by: $(F+G)(t)=F(t)+G(t)$ and is called *the sum* of $F$ and $G$.
- $kF:A\rightarrow\R^{n}$ is given by: $(kF)(t)=kF(t)$ and is the product of $F$ by the constant $k$.
- $f\cdot F:A\rightarrow\R^{n}$ is given by: $(f\cdot F)(t)=f(t)F(t)$ is the product of $F$ with the [[Scalar|scalar]] function $f$.
- $F \cdot G:A \rightarrow \R$ is the [[Dot Product|dot product]] of $F$ and $G$, defined as: $(F\cdot G)(t)=F(t)\cdot G(t)$.
All the properties such as commutativy, distributivity and others also apply.
Let $n=3$, in this case:
- $F \times G:A \rightarrow \R^{3}$ is the [[Cross Product]]  of $F$ and $G$, defined as $(F \times G)(t) = F(t)\times G(t)$:
$$\begin{align*}
F(t)&= \innp{F_{1}(t),F_{2}(t),F_{3}(t)}\\
G(t)&= \innp{G_{1}(t), G_{2}(t), G_{3}(t)}\\
F \times G&= 
\begin{vmatrix}
\hat{i} &  \hat{j} & \hat{k}\\
F_{1}(t) & F_{2}(t) & F_{3}(t)\\
G_{1}(t) & G_{2}(t) & G_{3}(t)
\end{vmatrix}\\
&= \hat{i}\det\begin{vmatrix}F_{2}(t) & F_{3}(t)\\ G_{2}(t) & G_{3}(t) \end{vmatrix}-\hat{j}\det\begin{vmatrix}F_{1}(t) & F_{3}(t) \\ G_{1}(t) & G_{3}(t)\end{vmatrix}
+ \hat{k}\det\begin{vmatrix}F_{1}(t) & F_{2}(t)\\ G_{1}(t) & G_{2}(t) \end{vmatrix}
\end{align*}$$
___
## Limits, Continuity and Derivatives

The formal definition of a limit can be found here: [[Epsilon-Delta Definition of a Limit|limit]], Here we just defined it for VVF's. As you probably guessed:
$$\begin{align*}
\lim_{t\rightarrow_{t_{0}}} F(t)=L \iff \forall\epsilon\gt0\,\exists\delta\gt0\mid\forall t\in D_{F},\,\,0\lt|t-t_{0}|<\delta\implies\norm{F(t)-L}\lt\epsilon
\end{align*}$$
This basically says that if i choose some [[Intervals|interval]] $\epsilon$ around the $L$ axis and collapse it closer and closer to $L$, there will be a interval $\delta$ such that $t-\delta$ and $t+\delta$ are arbitrarily close to $t$, *(but never reach $t$)* and the distance between vectors $F(t)$ and $L$ will be arbitrarily small as well, but never $0$, since we do not touch the actual $F(t)$ value. 

deltas are little input knobs we can calibrated to go around $t_{0}$ and epsilon will follow that calibration, hence we made the delta infinitesimally small and epsilon gets small too.

So after all this talk:
Let $F(t)= (F_{1},F_{2},\cdots,F_{n})$ be a vector valued function, 