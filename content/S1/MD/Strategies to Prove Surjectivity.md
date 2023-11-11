---
tags:
  - "#md"
  - proofs
aliases:
  - surjectivity
date: 2023-11-10
---
A Guideline of procedures to prove whether a [[Functions in Discrete Math|function]] is [[Surjective Functions|surjective]] or not.
___
1. Recall the definition of [[Surjective Functions]]:
$$\begin{align*}
\forall y\in\mathbb{Y}\;\exists x\in \mathbb{X}: f(x) &= y
\end{align*}$$
Where $\mathbb{X}$ is the [[Domain]] and $\mathbb{Y}$ is the [[Range in Discrete Math|range]].
___
2. Start the Proof 
>The process of this proof is pretty much thoroughly follow the definition and prove every step. Let's start with $y \in R$

Take the function $f: \mathbb{R} \implies \mathbb{R}$ defined by $f(x) = mx+b$ with $m\ne 0$ as example.

Since the function maps real numbers to real numbers we can safely assume that any $y$ in the range is a real number so start with:
$$y\in \mathbb{R}$$

- Now we have to show that there exists a $x$ in $\mathbb{X}$.
Let's find $x$:
$$\begin{align*}
f(x) &= y\\
mx+b&= y
\end{align*}$$
We replace $f(x)$ with the actual definition of the function. now we proceed to find $x$:
$$\begin{align*}
mx+b&= y\\
mx&= y-b\\
x&= \frac{y-b}{m}
\end{align*}$$
Since $m\ne0$ we can safely divide by $0$.
- Now we gotta show that $x = \frac{y-b}{m}$ is a real number. See:
	- $y \in \mathbb{R}$ 
	- $b \in \mathbb{R}$
	- We subtract $b$ from $y$ we get a real number
	- We divide by $m$ and since $m$ can't be zero we are with a real number.

- Now we just gotta show $f(x) = y$ 
Write down $f(x) = y$, and then we replace $x$ with what it actually is:
$$\begin{align*}\\
f(x) &= y \\
f\left(\frac{y-b}{m}\right)&= mx+b\\
&= m(\frac{y-b}{m})+b\\
&= \frac{m(y-b)}{m}+b\\
&= y-b+b\\
&= y
\end{align*}$$

#### Recall
The steps we took were:
- We started with a $y$ in the [[Codomain|codomain]];
- We showed there existed an $x$ in the domain;
- And then we showed there existed an $x$ such that $f(x)=y$.