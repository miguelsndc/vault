---
tags:
  - propositional-logic
aliases:
  - if and only if
  - iff
  - biconditional statements
date: 2023-10-26
---
Let $p$ and $q$ be [[Proposition|propositions]]. The *biconditional statement* $p \iff q$ is true when $p$ and $q$ have the same truth values, otherwise it's false. it's also called *bi-implication*.
It's basically $(p \implies q) \land (q \implies p)$. simplified as $p \iff q$, See the arrow pointing to both sides.
#### Truth Table

| p   | q   | $p \iff q$ | $(p \implies q) \land (q \implies p)$ |
| --- | --- | ---------- | ------------------------------------- |
| F   | F   | T          | T                                     |
| F   | T   | F          | F                                     |
| T   | F   | F          | F                                     |
| T   | T   | T          | T                                     |
*last column added for visualization purposes.*
##### Terminology
- "$p$ is necessary and sufficient for $q$"
- "If $p$ then $q$, conversely".
- "$p$ iff $q$" with **iff** being an abbreviation for *if and only if*.