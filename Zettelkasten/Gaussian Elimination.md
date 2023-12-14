---
tags: systems
---
Gaussian elimination is an algorithm for solving $n\times n$ [[Definition of a System of Linear Equations|system of linear equations]], this means *number of equations $=$ number of variables*,
We multiply and add the equations in order to eliminate the unknowns, from a $n \times n$ system we get a smaller $n - 1 \times n - 1$ system, and we keep doing this until we have a $1 \times 1$ system which we can immediately solve. Once we find this value, we solve for the other equations and keep doing this until all unknowns are found.

>[!important] When does it fail ?
>If one of the pivots happen to be zero, then the elimination technique cannot proceed, otherwise, there is only one solution and it can be found via [[Back-Substitution]] and elimination.



