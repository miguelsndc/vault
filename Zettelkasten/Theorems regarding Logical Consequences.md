---
tags: logic
---

>**Lemma**: Let $\Gamma = \{\alpha_{1},\alpha_{2},\cdots,\alpha_{n}\}$, if $\Gamma \vDash \phi$ ($\phi$ is a [[Satisfiability|logical consequence]] of $\Gamma$), then $\Gamma \cup \{(\neg \phi)\}$ is [[Satisfiability|unsatisfiable]].

## Proof
We want to prove that $\Gamma \vDash \phi \implies \Gamma \cup \{(\neg \phi)\}$ is UNSAT.

1. Suppose $\Gamma \vDash \phi$ where $\Gamma = \{\alpha_{1},\alpha_{2},\cdots,\alpha_{n}\}.$
2. In this case $\forall v, \, \hat{v}(\alpha_{1},\alpha_{2},\cdots,\alpha_{n})=1$ 