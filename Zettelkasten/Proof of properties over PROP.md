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
	- Inductive hypothesis $f(\rho) +f(\theta ) \le g(\rho) + g(\theta)$, where $\Box = \{\implies, \lor, \land\}$.
	- Thesis: $f(\rho \,\Box\, \theta) \le g(\rho \, \Box \, \theta)$
By the definitions of the functions themselves:
$$\begin{align*}
f(\rho \,\Box\, \theta)&= \max(f(\rho),f(\theta)) + 1\\
g(\rho \,\Box\, \theta)&= g(\rho)+g(\theta)+1
\end{align*}$$We want to show that:
$$\begin{align*}
\max(f(\rho),f(\theta)) + 1 \le g(\rho)+g(\theta)+1
\end{align*}$$
By the definition of $\max$, and since $f$ can't output negative values, $\max(f(\rho),f(\theta)) \le f(\rho) + f(\theta)$, and by the $I.H$ $f(\rho) + f(\theta) \le g(\rho) + g(\theta)$, and $1 \le 1$, by transitivity, $\max(f(\rho), f(\theta)) + 1\le g(\rho) + g(\theta) + 1$.

> **Lemma**: For all propositions $\phi \in PROP$, the number of [[Recursive Functions over PROP|subexpressions]] of $\phi$ is at most $2n + 1$ where $n$ is the number of operators of $\phi$.

We want to show that for all $\phi \in PROP$, $|s(\phi)| \le 2f(\phi) +1$. where $||$ represents the [[Cardinality]] of a [[Sets|set]], since $s(\phi)$ outputs a set, not a number.

- Base case: ($\phi$ is atomic), in this case: $s(\phi) = \{\phi\}$ and $|s(\phi)| = 1$, and $f(\phi)= 0$, so $2f(\phi) + 1= 2*0 + 1 = 1$, and $1\le 1$, so the base case holds.
- Inductive step:
	- Hypothesis: $|s(\psi)| \le 2f(\psi) + 1$.
	- Thesis: $|s((\neg \psi))| \le 2f((\neg\psi)) + 1$ 
By definition, $s((\neg\psi))=s(\psi)\cup\{\psi\}$ and $f((\neg\psi)) = f(\psi) + 1$, therefore:
$$\begin{align*}
|s(\psi) \cup \{\psi\}\ | &= |s(\psi)| +|\{\psi\}| - |s(\psi) \cap \{\psi\}|\\
\end{align*}$$
and $2f((\neg\psi))+1 = 2(f(\psi) + 1) + 1= 2(f(\psi)) +1+2$, So we want to show that:
$$\begin{align*}
|s(\psi)| +|\{\psi\}| - |s(\psi) \cap \{\psi\}| &\le 2f(\psi) + 1 + 2\\
|s(\psi)| + |\{\psi\} - |\{\psi\} \cap \{\psi\}| &\le 2(f(\psi)) + 1 + 2\\
|s(\psi)|&\le 2f(\psi)+1+2
\end{align*}$$
By the I.H, $|s(\psi)| \le 2f(\psi) + 1$, and obviously, $|s(\psi)| \le 2f(\psi) + 1 + 2$.
- Inductive step:
	- Hypothesis: $(1)$ $|s(\rho)| \le 2f(\rho) + 1$; $(2)$ $|s(\theta)| \le 2f(\theta) + 1$.
	- Thesis: $|s(\rho \sqsep \theta)| \le 2f(\rho \sqsep \theta)+1$ where $\sqsep = \{\implies, \lor, \land\}$.
By the definitions, we want to show that:
$$\begin{align*}
|s(\rho \sqsep \theta)| &\le2f(\rho \sqsep \theta)+1\\
|s(\rho)\cup s(\theta)\cup \{(\rho \sqsep \theta)\}| &\le 2(f(\rho)+f(\theta)+1)+1
\end{align*}$$