---
tags: logic
---
Here we state some lemmas about the properties of $PROP$, using the functions defined in [[Recursive Functions over PROP]].

**Lemma:** *For all propositions $\phi \in PROP$, the number of parentheses of $\phi$ is even*
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