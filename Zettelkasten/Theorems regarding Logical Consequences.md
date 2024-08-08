---
tags: logic
---

>**Theorem**: Let $\Gamma = \{\alpha_{1},\alpha_{2},\cdots,\alpha_{n}\}$, if $\Gamma \vDash \phi$ ($\phi$ is a [[Satisfiability|logical consequence]] of $\Gamma$), if and only if $\Gamma \cup \{(\neg \phi)\}$ is [[Satisfiability|unsatisfiable]].

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
$(b)$ $\Gamma \cup \{(\neg \phi)\} \implies \Gamma \vDash \phi$ 
1. Suppose $F \cup \{(\neg \phi)\} = \{\alpha_{1}, \cdots, \alpha_{n}, \neg \phi\}$ is unstafisfiable, that means:
2. $\forall v, \, \hat{v}((\alpha_{1}\land\alpha_{2}\land \cdots\land \alpha_{n}) \land (\neg\phi)))=0$, if we negate:
3. $\forall v, \, \hat{v}(\neg (\alpha_{1}\land \cdots \land \alpha_{n}) \lor \phi)= 1$  
4. $\forall v, \, \hat{v}((\alpha_{1}\land \cdots \land \alpha_{n}) \implies \phi)= 1$  
5. Therefore $\Gamma \vDash \phi$.

> **Theorem**: Let $\phi$ be a [[Proposition]], $\phi$ is [[Satisfiability|satisfiable]] [[If and Only if]], $\neg \phi$ is [[Satisfiability|refutable]].

# Proof
$(a)$ $\phi$ satisfiable $\implies$ $\neg \phi$ refutable:

1. Suppose that $\phi$ is satisfiable, this means that $\exists v, \mid \hat{v}(\phi)=1$, let $f$ be that [[Valuation]].
2. This implies that $\hat{f}((\neg\phi)) \rightarrow \f{NEG}(\hat{f}(\phi))$ since $\hat{f}(\phi) = 1$, this means that $\hat{f}(\neg \phi)= 0$.
3. Therefore $\neg\phi$ is refutable.  

$(a)$ $\neg\phi$ refutable $\implies$ $\phi$ satisfiable:

1. Suppose that $\neg \phi$ is refutable, therefore $\exists v \mid \hat{v}((\neg \phi))=0$, let $f$ be that [[Valuation]] 
2. This implies that, since $f((\neg \phi)) = \f{NEG}(\hat{f}(\phi))=0$, this means that:  
3. If we negate both sides of $\f{NEG}(\hat{f}(\phi))=0$ we obtain $\hat{f}(\phi) = 1$.
4. Therefore $\phi$ is satisfiable