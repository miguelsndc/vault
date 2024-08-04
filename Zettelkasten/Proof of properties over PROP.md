---
tags: logic
---
Here we state some lemmas about the properties of $PROP$, using the functions defined in [[Recursive Functions over PROP]].

> **Lemma:** *For all propositions $\phi \in PROP$, the number of parentheses of $\phi$ is even*

**Proof**:
We want to prove that for all $\phi$, $f(\phi)$ is even where $f$ is the number of parentheses function.
- Base case ($\phi$ is atomic)
By the definition of $f$, $f(\phi) =0$ and $0$ is even.
- Inductive step
	- Inductive Hypothesis: $f(\psi)$ is even
	- Thesis $f((\neg \psi))$ is even.
$f((\neg \psi))$ is defined as $f(\psi) + 2$, and by the I.H $f(\psi)$ is even, therefore $f(\neg \psi)$ is even.

- Inductive step ($\phi$ is like $\rho \, \square \, \theta$ where $\square = \{\implies, \lor, \land\}$) 
	- Inductive Hypothesis $(1)$: $f(\rho)$ is even
	- Inductive Hypothesis $(2)$: $f(\theta)$ is even
- Thesis: $f(\rho \, \square \, \theta)$ is even. 
$f(\rho \, \square \, \theta)$ is defined as $f(\rho) + f(\theta) + 2$, by the I.H, $f(\rho)$ and $f(\theta)$ are even, therefore $f(\rho \, \square \, \theta) = f(\rho) + f(\theta) + 2$ is also even, thus the thesis is proven.

The proof is complete.

> **Lemma**: For all propositions $\phi \in PROP$, the rank of $\phi$ is at most the number of operators of $\phi$.

**Proof**:
We want to prove that $f(\phi) \le g(\phi)$ for all propositions $\phi$ where $f$ is the rank of $\phi$ and $g$ is the number of operators of $\phi$.
- Base case: ($\phi$ is atomic), in this case $f(\phi) = 0$ and $g(\phi) = 0$, and $0 \le 0$, so the base case holds.
- Inductive step:
	- Inductive Hypothesis: $f(\psi) \le g(\psi)$
	- Thesis: $f((\neg \psi)) \le g((\neg \psi))$
By the definition of the functions themselves we have that:
$$\begin{align*}
f((\neg \psi)) &= f(\psi) + 1\\
g((\neg \psi)) &= g(\psi) + 1\\
\end{align*}$$
By the I.H $f(\psi) \le g(\psi)$ and since $1 \le 1$ the thesis is proven.
- Inductive step:
	- Inductive hypothesis $f(\rho) +f(\theta ) \le g(\rho) + \Box \, \theta)$  where $\Box = \{\implies, \lor, \land\}$.
	