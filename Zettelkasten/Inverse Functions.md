---
tags:
  - functions
aliases:
  - inverse
date: 2023-11-13
---
Now consider a [[Bijective|bijection]] $f$ from [[Sets|set]] $A$ to $B$. Because $f$ is [[Surjective Functions|surjective]] then every element of $B$ is the image of some element in $A$. Furthermore, because $f$ is also a [[Injective Functions|one-to-one]] function, we a guaranteed that every element of $B$ is the image of a *unique* element in $A$. Consequently, we can define a new function from $B$ to $A$ that reverses the correspondence of $f$.
#### Definition
Let $f$ be a [[Bijective|bijection]] from set $A$ to B. The **inverse function** of $f$ is the function that assigns to an element $b \in B$ a unique element in $a \in A$ such that $f(a) = b$. The inverse function of $f$ is denoted by $f^{-1}$. Hence $f^{-1}(b) = a$ when $f(a) = b$.