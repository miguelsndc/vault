---
tags:
  - md
  - propositional-logic
aliases:
  - logical operators
date: 2023-10-25
---
Based on [[Proposition]], we can use some operators to create more complex propositions based on others, See:
- $p\lor q$, $p$ or $q$
	- Yields true whether one (or both) propositions are **true**.
- $p\land q$, $p$ and $q$
	- Yields true if both propositions are **true**
- $p\oplus q$ $p$ xor $q$
	- Yields true if only **one of** the propositions are true, neither both **true** or **false** will satisfy $xor$.
- $\neg p$, not $p$ 
	- Negate the proposition $p$. If $p$ is true, it becomes false and vice-versa
- $p \implies q$, If $p$ then $q$. $p$ implies $q$ 
	- Is a relationship of two proposition when one is last is a logical consequence of the first $p$ is called the *premise* and $q$ is called the *conclusion*. **False only when $p$ is true and $q$ is false, Otherwise always true.**
- $p \iff q$, $p$ if and only if $q$.
	- Bothways implication, expressed as $(p\implies q) \land (q \implies p)$. True when $p$ and $q$ are equal.