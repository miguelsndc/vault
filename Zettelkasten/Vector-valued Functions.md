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
Let $F= (F_{1},F_{2},\cdots,F_{n})$ be a vector valued function, and $L=(L_{1},L_{2},\cdots,L_{n}) \in R^{n}$, so:
$$\begin{align*}
\lim_{t\rightarrow t_{0}}F(t)=L\iff \lim_{t \rightarrow t_{0}}F_{i}(t)=L_{i},\,\, i=1,2,\cdots,n
\end{align*}$$
The limit only exists if the limit of every component function of $F$ also exists and is equal to the matching component of $L$, so, naturally, $F$ is [[Differentiability and Continuity|continuous]] at $t_{0}$ if $\lim_{t \rightarrow t_{0}}F(t)=F(t_{0})$.

## Derivatives

Since the notion of [[Epsilon-Delta Definition of a Limit|limit]] is well-stablished, [[Derivative Definition|derivatives]] are no different, the derivative of a VVF $F:A \rightarrow \R^{n} :=F(t)=(F_{1}(t),\cdots,F_{n}(t))$, defined as $F'(t)= \frac{dF}{dt}=(F_{1}'(t),\cdots,F_{n}'(t))$. The derivative of $F$ is the derivative of each component.

## Tangent lines
Geometrically, 0the vector $\frac{dF}{dt}(t_{0})$ is the *"tangent vector"* to the trajectory of $F$ at the point $t_{0}$.
![[tangent vector.excalidraw]]
Here we see that the vector $F(t) - F(t_{0})$ is parallel to $\frac{F(t)- F(t_{0})}{t- t_{0}}$, when $t \rightarrow t_0$, $\frac{F(t)- F(t_{0})}{t- t_{0}}$ converges to the "tangent vector" $\frac{dF}{dt}(t_{0})$ to the trajectory of $F$ in $F({t_0})$.

The blue dashed line passing through $\frac{dF}{dt}(t_{0})$ is the tangent [[Parametric Lines|line]] to the trajectory of $F$ at $t_{0}$, defined as:
$$\begin{align*}
X(\lambda)&= F(t_{0})+\lambda \frac{dF}{dt}(t_{0})
\end{align*}$$
Is just a [[Parametric Lines|parametric line]].

Let $\vec{F}, \vec{G}:A \rightarrow \R^{n}, f:A\rightarrow\R$ be all [[Differentiability and Continuity|differentiable]] in $A$, so:
- $\frac{d}{dt}(f\cdot \vec{F})=\frac{df}{dt}\cdot \vec{F}+ f\cdot \frac{d\vec{F}}{dt}$.
- $\frac{d}{dt}(\vec{F}\cdot\vec{G})= \frac{d\vec{F}}{dt}\cdot \vec{G}+ \vec{F}\cdot \frac{d\vec{G}}{dt}$
-  Let $n=3$; $\frac{d}{dt}(\vec{F} \times \vec{G})= \frac{d\vec{F}}{dt}\times \vec{G}+ \vec{F}\times \frac{d\vec{G}}{dt}$ 
Are also [[Differentiability and Continuity|differentiable]] in $A$.