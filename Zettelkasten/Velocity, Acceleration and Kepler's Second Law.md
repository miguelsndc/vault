---
tags: vector
---
**Position**: The position vector $\vec{r}(t)$ tells us the trajectory of a moving point in space with respect to time, it's the vector from the origin all the way to the point $\vec{r}(t)$.

**Velocity**: The velocity vector $\vec{v}$ tells **how fast** you're going in a certain trajectory and it also tells in which direction you're going, which is useful information if you're trying to figure out where you're going:
$$\begin{align*}
\vec{v}=\frac{d \vec{r}}{dt}\\
\end{align*}$$
The velocity [[Vector]] is the [[Derivative Definition|derivative]] of **position** with respect to **time**, it makes sense since, how fast you're changing position is in fact how fast you're moving and to which direction.

**Speed**: Is a [[Scalar]] quantity, which is just the [[Vector Norm|magnitude]] of the vector $\vec{v}$.

**Acceleration**: is the derivative of **velocity** with respect to time $\vec{a} = \frac{d\vec{v}}{dt}$. *If the speed is constant, i.e the velocity vector is constant, this does not mean the acceleration is zero, the velocity vector can still **rotate** while maintaining the same magnitude, and that rotation produces acceleration.*

## Arc Length

The distance you have traveled along the curve is theintegral of the speed over time yields the arc length along the trajectory of a curve. $s=$ *distance traveled along the trajectory*

For that to make sense we need to fix a reference point from which we start measuring the distance, the arc length can perfectly be negative or positive, it is negative usually when counting before the reference point and positive afterwards.

![[arclength.excalidraw]]

From this picture we can infer the arc length being the sum of all the length of all the vectors between the points $P_{i-1}$ and $P_{i}$, if we let the distance $\Delta x$ between the points tend to zero, that will be actually the derivative of the curve at that point, and the distance will be the length of the tangent vector, so:  

$$\begin{align*}
\sum\limits_{i=1}^{n} [P_{i-1}, P_{i}] \implies \sum\limits_{i=1}^{n}||\innp{P_{i}-P_{i-1}}|| \implies\sum\limits_{i=1}^{n}||r'(i)|| \implies \lim_{\text{max} \Delta x \rightarrow 0} \sum\limits_{i=1}^{n}||r'(i)||\Delta x \implies \int_{0}^{p}||r'(t)||dt
\\\end{align*}$$
We bring up $\Delta x$ as the tiny steps in time we take, since $distance=speed \cdot time$, we need to multiply by a step in time, otherwise we'd just be summing speeds for the sake of summing speeds, there isn't much relevant information on saying we traveled $800 \frac{km}{h}$ without the time.

By letting the number of pairs $(P_{i-1}, P_{i})$ tend to infinity we naturally arrive at the integral of the speed with respect to time, so the arc length is just the infinite sum of the lengths of the tangent vectors at each point of the curve.

**Unit tangent vector**: at any point the velocity vector is tangent to the trajectory, it tells us the direction of motion, the unit tangent vector is $\hat{T}=\frac{\vec{v}}{||\vec{v}||}$ represents that direction. *(we could use the regular velocity vector to represent direction but why if the calculations are much easier with unit vectors ? a vector represents a displacement with direction and magnitude, a unit vector represents just direction and can be easily scaled to suit any needs)*. 

## Relationships between the different vector quantites and magnitudes seen 

$$
\vec{v}=\frac{d\vec{r}}{dt}=\frac{d\vec{r}}{ds}\cdot \frac{ds}{dt} = \hat{T} \frac{ds}{dt}=\hat{T} ||\vec{v}||
$$
![[drds.excalidraw]]

The vector between two points in the trajectory $r(t)$ and $r(t + \Delta t)$ is $\Delta\vec{r}$, and the distance traveled is $\Delta s$. $\frac{\Delta s }{\Delta t}$ is the $\frac{distance}{time} \approx speed$. and $\Delta\vec{r} \approx \hat{T} \Delta s$ . 

$$\begin{align*}
\Delta \vec{r}\approx\hat{T} \Delta s\\
\frac{\Delta \vec{r}}{\Delta t}\approx\hat{T} \frac{\Delta s}{\Delta t}
\end{align*}$$
By taking the limit as $\Delta t \rightarrow 0$ it becomes an equality instead of just an approximation, as we take smaller and smaller steps in time