---
tags: logic
---
Some useful concepts pop up when we discuss [[Valuation]] in [[Proposition|propositions]]:

Let $\phi$ be a proposition:
- $\phi$ is **satisfiable** if there exists a valuation $v$ that satisfies it, i.e, $\hat{v}(\phi) = 1$.
- $\phi$ is **refutable** if there exists a valuation $v$ that refutes it, i.e $\hat{v} =0$
- $\phi$ is a [[Tautology]] if all valuations satisfy it.
- $\phi$ is **unsatisfiable** if all valuations refute it.
Let $\psi$ be a proposition:
- $\phi$ and $\psi$ are **logically equivalent** or just **equivalent** if, for all valuations $v$, $\hat{v}(\phi) = \hat{v}(\psi)$.
Let $\Gamma$ be a [[Sets|set]] of propositions;
- $\Gamma$ is satisfiable or **consistent** if there exists a valuation that satisfies all it's propositions.
- $\Gamma$ is **unsatisfiable** or **inconsistent** if there's no valuation that satifies all it's propositions.
- $\phi$ is **logical consequence** of $\Gamma$ $(\Gamma \vDash \phi)$ if all valuations that satisfy $\Gamma$ also satisfy $\phi$. 
Let $\Gamma = \{\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}\}$, we say that $\psi$ is a logical consequence of $\Gamma$ if:
$$\begin{align*}
(\alpha_{1} \land \alpha_{2}\land \cdots \land \alpha_{n})\implies \psi
\end{align*}$$
