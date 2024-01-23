	---
tags: functions
aliases: floor, ceil, ceiling
---
A Floor function assigns to any [[Real Numbers|real number]] $x$ the closest integer less than or equal to $x$.
A Ceil function assigns to any real number $y$ the closest integer greather than or equal to $y$.
Floor: $\lfloor 2.1 \rfloor = 2$
Ceil $\lceil 2.1 \rceil = 3$.
## Useful Properties of Ceiling and Floor functions
- $\lfloor x\rfloor=n$ if and only if $n \le x \lt n + 1$
- $\lceil x\rceil=n$ if and only if $n - 1\lt x \le n$
- $\lfloor x\rfloor=n$ if and only if $x - 1 \lt n \le x$ 
- $\lceil x\rceil=n$ if and only if $x \le n \lt x + 1$
- $x - 1 \lt \lfloor x \rfloor \le x \le \lceil x \rceil \lt x + 1$.
- $\lfloor - x \rfloor = - \lfloor x\rfloor$   
- $\lceil - x \rceil= - \lceil x\rceil$
- $\lceil x + n \rceil= \lceil x\rceil + n$
- $\lfloor x + n \rfloor = \lfloor x \rfloor + n$