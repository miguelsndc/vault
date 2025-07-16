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

so given $S$ as a simple polygon enclosing a set of points $P$, assume by contradiction that $S$ is the smallest perimeter polygon enclosing $P$, and there is at least one concave vertex $B$, whose is between two other vertices $A$ and $C$, so $B$ by definition has a inward angle greater than 180, given that this vertex is $B$ and its neighbours are $A$ and $C$, by the triangle inequality:
$$\begin{align*}
|AB| + |BC| > |AC|
\end{align*}$$
So take $S'$ formed by replacing edges $(A,B), (B,C)$ with the edge $(A,C)$, the perimeter of $S$ is strictly less than $S$'s, and we can apply the same argument for every concave vertex in $S'$, once obtaining a polygon without concave vertices, therefore being convex, contradicting our assumption that $S$ was the smallest perimeter polygon, and showing that the polygon we get must be convex.

$c)$ Okay so since $\rm conv(S)$ is by definition the intersection of all convex sets containing $S$, it follows that $\rm conv(S) \subseteq C$. where $C$ is any arbitrary convex hull containing the points of $S$.

$1.2)$ "The polygon $P$ (the convex hull of the set $'P$) can only be formed by the **extreme vertices** of $P'$. Since the set of extreme points is **uniquely defined** by $P′$, the polygon $P$ is uniquely determined.

Furthermore, $P$ is the **intersection of all convex sets** containing $P'$, because every convex set that contains $P'$ must also contain the extreme points of $P'$, and thus must contain their convex hull."