---
tags: logic
---
Since [[PROP is Freely Generated]], $PROP$ being the [[Inductive Sets and Closures|inductive closure]] of all expressions of #propositional-logic  and thus representing the [[Sets|set]] of all legitimate expressions; We can define **recursive** functions over $PROP$, since it has the property of unique reading, implying that the process of defining recursive functions over it is mathematically safe.

As notation we'll use the greek letters $\phi,\psi, \rho$ and $\theta$ to represent the expressions.

## Number of parenthses

$f: PROP \rightarrow \N$ 
$f(\phi) = 0$ if $\phi$ is atomic, i.e $\phi \in X$ where $X$ is the [[Theorems and Proofs for Basis and Dimension|basis]].
$f((\lnot \psi))= f(\psi) + 2$;
$f((\rho \land \theta))= f(\rho) + f(\theta) + 2$;
$f((\rho \lor \theta)) = f(\rho) + f(\theta) + 2$;
$f((\rho \implies \theta)) = f(\rho) + f(\theta) + 2$;

Atomic expressions do not contribute to the number of parentheses of an expression, while every operator contributes with $2$ parentheses, see the example for $f((x \lor (\lnot y))) = f(x) + f(\lnot y) + 2 = f(x) + f(y) + 2 + 2= 0+0 +2+2=4$. 
