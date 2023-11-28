---
tags:
  - propositional-logic
  - proof-methods
aliases:
  - contrapositive
date: 2023-10-26
---
The contrapositive is one of the three operations that can be derived from the [[Implication]], being defined as $\neg q \implies \neg p$. **It's the only operation that has the same truth values as $p \implies q$. See:**
___ 
The only way for $\neg q \implies \neg p$ to be false is when $\neg q$ is true and $\neg p$ is false, that is, when $p$ is true and $q$ is false. We will show that neither the [[Converse]] nor the [[Propositional Inverse|inverse]] have the same truth values.
#### Truth Table
| p   | q   | $p \implies q$ | $\neg q \implies \neg p$ |
| --- | --- | -------------- | ------------------------ |
| F   | F   | T              | T                        |
| F   | T   | T              | T                        |
| T   | F   | F              | F                        |
| T   | T   | T              | T                         |
