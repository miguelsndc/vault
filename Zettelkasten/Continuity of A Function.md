---
tags:
- function
- limits
aliases: continuity
---
In [[Epsilon-Delta Definition of a Limit|limits]] we discuss what happens when a [[Functions in Discrete Math|function]] $f$ approaches a point $p$, it is not necessary that $f$ exists at $p$ since in the definition we state that $x \ne p$, but, for a limit $lim_{x\to p}f(x)=A$ when the limit **exists** at $p$ and is indeed equal to $A$ we say that **$f$ is continuous at $p$**, $i.e$ we have the definition:

>[!tip] Definition of Continuity of a Function at a Point
>*a function $f$ is said to be continuous at a point $p$ if:*
>(a) $f$ is defined at $p$ and
>(b) $\lim_{x\to p}f(x) = f(p)$ 
>

In terms of the [[Epsilon-Delta Definition of a Limit]], the definition can be restated as follows:
>[!tip] In Terms of Epsilon-Delta
>a function $f$ is continuous at $p$ if for every $\epsilon \gt 0$ there is a $\delta \gt 0$ such that
>$|f(x) - f(p)| \lt \epsilon$ whenever $|x-p| \lt \delta$ 
>Note that we don't need the $x\ne p$ constraint.

