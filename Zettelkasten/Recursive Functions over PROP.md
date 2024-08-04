---
tags: logic
aliases: parentheses, operators, subexpression, subexpressions, operator, operators, rank, posto, tree, syntax tree, syntax
---
Since [[PROP is Freely Generated]], $PROP$ being the [[Inductive Sets and Closures|inductive closure]] of all expressions of #propositional-logic  and thus representing the [[Sets|set]] of all legitimate expressions; We can define **recursive** functions over $PROP$, since it has the property of unique reading, implying that the process of defining recursive functions over it is mathematically safe.

As notation we'll use the greek letters $\phi,\psi, \rho$ and $\theta$ to represent the expressions.

## Number of parentheses

$f: PROP \rightarrow \N$ 
$f(\phi) = 0$ if $\phi$ is atomic, i.e $\phi \in X$ where $X$ is the [[Definitions of Logic|basis]] .
$f((\lnot \psi))= f(\psi) + 2$;
$f((\rho \land \theta))= f(\rho) + f(\theta) + 2$;
$f((\rho \lor \theta)) = f(\rho) + f(\theta) + 2$;
$f((\rho \implies \theta)) = f(\rho) + f(\theta) + 2$;

Atomic expressions do not contribute to the number of parentheses of an expression, while every operator contributes with $2$ parentheses, see the example for $f((x \lor (\lnot y))) = f(x) + f(\lnot y) + 2 = f(x) + f(y) + 2 + 2= 0+0 +2+2=4$. 

## Number of operators

$f: PROP \rightarrow \N$ 
$f(\phi) = 0$ if $\phi$ is atomic, i.e $\phi \in X$ where $X$ is the basis.
$f((\lnot \psi)) = f(\psi) + 1$
$f((\rho \lor \theta)) = f(\rho) + f(\theta) + 1$
$f((\rho \land \theta)) = f(\rho) + f(\theta) + 1$
$f((\rho \implies \theta)) = f(\rho) + f(\theta) + 1$

Atomic expressions do not contribute to the number of operators because there are no operators at all within them. every generator function contributes with $1$ operator, it's own.

## Number of Symbols

$f:PROP \rightarrow \N$ 
$f(\phi) = 1$ if $\phi$ is atomic, i.e $\phi \in X$ where $X$ is the basis.
$f((\lnot \psi)) = f(\psi) + 3$
$f((\rho \lor \theta)) = f(\rho) + f(\theta) + 3$
$f((\rho \land \theta)) = f(\rho) + f(\theta) + 3$
$f((\rho \implies \theta)) = f(\rho) + f(\theta) + 3$

Atomic expressions contribute with $1$ to the count of total symbols, the functions contribute with $3$ symbols, the two parantheses and the operator.

## Subexpressions

Subexpressions are the [[Sets|set]] containing the individual pieces of each expression, the atomic expressions, each operator and it's argument, as well as the whole expression, since a set is always [[Subsets|subset]] of itself.

$s: PROP \rightarrow P(PROP)$ where $P$ is the [[Power Set]].
$s(\phi) = \{\phi\}$ where $\phi$ is an atomic expression.
$s((\lnot \psi)) = s(\psi) \cup \{(\lnot \psi)\}$ 
$s((\phi \lor \theta)) = s(\phi) \cup s(\theta) \cup \{(\phi \lor \theta)\}$ 
$s((\phi \land \theta)) = s(\phi) \cup s(\theta) \cup \{(\phi \land \theta)\}$ 
$s((\phi \implies \theta)) = s(\phi) \cup s(\theta) \cup \{(\phi \implies \theta)\}$ 

Every subexpression contributes with itself plus it's own subexpressions to the [[Sets|set]], so, for example: $s((x \lor (\lnot y)))= \{x, y, (\lnot y), (x \lor (\lnot y))\}$. 

## Syntax Tree

> Can't write trees on obsidian.

![[Pasted image 20240803193206.png]]

So each atomic expression contributes with a node containing itself, and every operator contributes with a subtree with the operator at the root and it's children being the subexpressions within.

## Rank (Posto)
Rank is the height of the syntax tree of an expression.

$p: PROP \rightarrow \N$ 
$p(\phi) = 0$ if $\phi$ is an atomic expression.
$p((\neg \psi) = p(\psi) + 1$ 
$p((\rho \lor \theta)) = max(p(\rho), p(\theta)) + 1$  
$p((\rho \land \theta)) = max(p(\rho), p(\theta)) + 1$  
$p((\rho \implies \theta)) = max(p(\rho), p(\theta)) + 1$  

A atomic expression only adds a node to the tree, therefore not contributing to the total height, every operator adds $1$ to the total count, since the operator has it's children as the subexpressions. for example, $p((x \lor (\neg y))) = max(p(x), p(\neg y))+ 1 = max(p(x), p(y) + 1) + 1 = max(0, 1) + 1 = 1 + 1 = 2$  