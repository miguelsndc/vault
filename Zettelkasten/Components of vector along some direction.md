---
tags: vector
aliases: component
---
![[compoents]]
Let's say we want to find the component of $a$ along the direction $u$ *($u$ is a unit vector)*, the length of the red segment is $\norm{a}\cos{\theta}$, since $u$ is unitary that equals $\norm{a} \norm{u} \cos{\theta}=a \cdot u$. 

> "Component" is the length of projection of $a$ along some direction $u$ (unitary vector). 

If we want to find the component across the $\hat{i}$ direction we compute $a\cdot\innp{1,0,0}= \innp{a_{1},0,0}$ which is the component across the $x$-axis, the same works for $y$ and $z$ axis, for some arbitrary axis defined by some unit vector, that component is $a \cdot u$ as shown above.

If $u$ is not a unit vector we can just use the [[Projection onto a line]] formula. If $u$ is unitary, the vector in $u$ direction with the same length as $a$ is just $(a \cdot u)u$.