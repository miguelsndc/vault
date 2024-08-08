---
tags: logic
---

>**Lemma**: Let $\Gamma = \{\alpha_{1},\alpha_{2},\cdots,\alpha_{n}\}$, if $\Gamma \vDash \phi$ ($\phi$ is a [[Satisfiability|logical consequence]] of $\Gamma$), if and only if $\Gamma \cup \{(\neg \phi)\}$ is [[Satisfiability|unsatisfiable]].

## Proof
We want to prove that $\Gamma \vDash \phi \iff \Gamma \cup \{(\neg \phi)\}$ is UNSAT.

$(a)$ $\Gamma \vDash \phi \implies \Gamma \cup \{(\neg \phi)\}$
1. .Suppose $\Gamma \vDash \phi$ where $\Gamma = \{\alpha_{1},\alpha_{2},\cdots,\alpha_{n}\}.$
2. In this case $\forall v, \, \hat{v}(\alpha_{1}\land\alpha_{2}\land\cdots\land\alpha_{n})=1 \implies \hat{v}(\phi)= 1$.
3. $\forall v, \, \hat{v}((\alpha_{1}\land\alpha_{2}\land \cdots\land \alpha_{n}) \implies \phi) =1$
4. $\forall v, \, \hat{v}(\neg(\alpha_{1}\land\alpha_{2}\land \cdots\land \alpha_{n}) \lor \phi)=1$
5. $\forall v, \, \hat{v}(\neg(\neg(\alpha_{1}\land\alpha_{2}\land \cdots\land \alpha_{n}) \lor \phi))=0$ 
6. $\forall v, \, \hat{v}((\alpha_{1}\land\alpha_{2}\land \cdots\land \alpha_{n}) \land (\neg\phi)))=0$  
7. Therefore $\{\alpha_{1}, \alpha_{2},\cdots,\alpha_{n}\} \cup \{(\neg \phi)\}$ is unsatisfiable, hence, $\Gamma \cup \{(\neg \phi)\}$ is unsatisfiable.
$(b) \Gamma \cup \{(\neg \phi)\} \implies $