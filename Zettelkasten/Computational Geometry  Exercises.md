---
tags: geometry
---

### 1.5 Exercises

$1)$ Let $P$ and $Q$ be two convex sets, also let $R = P \cap Q$, let $p$ and $q$ be two points in $R$, and $\overline{pq}$ be the segment between them. Assume by contradiction that $R$ is not convex, so there is some point $x$ along $\overline{pq}$ that is not contained in $R$, so $x \notin R \implies$ $x\notin P$ or $x \notin Q$

But since $p, q \in P$ and $P$ is convex, all points along the segment $\overline{pq}$ are contained in $P$, so $x \in P$
And also $p, q \in Q$ and $Q$ is convex, all points along the segment $\overline{pq}$ are contained in $Q$ and $x \in Q$

so $x \in P \cap Q$, contradicting our assumption, therefore $R$ must be convex.

$2)$ The perimeter of a polygon is defined as the sum of lengths of the edges between two consecutive vertices, we aim to show that the smallest perimeter polygon enclosing a set of points is convex. First we need to:

1. Figure out the smallest perimeter polygon enclosing a set of points is and what makes it the "smallest".

2. Given the smallest perimiter polygon, show it is convex.

so i found out by drawing that if i make a "shell" around the points, notice that if i have three points making a triangle, it is always better to connect the two upmost points rather than connecting with the inner one, we can find that out via hypot formula, we expand and get that $a + b > c$ so we should take c, this guarantees we do not take any "left turns"on the shell, leaving spikes that create concave polygons.

i have no clue how to prove it this was the most promising idea i've had



___

