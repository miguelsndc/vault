---
tags: logic
aliases: alphabet, syntax, language
---
Here we provide some basic definitions of logic. 
- **Consistent [[Sets|set]]**: A set where there is at least one case where the [[Proposition|propositions]] line up and all become true. See the example:
	- $X$ says $B$ is guilty.
	- $Y$ says that $C$ is guilty
	- $Z$ says that A is guilty
	- If this set is consistent, there is at least one solution for this [[Definition of a System of Linear Equations|system of equations]].
$$\begin{align*}
\begin{cases}
X \land {\lnot}Y&= 1\\
Z \implies Y&= 1\\
\lnot Y \land (X \lor Y)&= 1 
\end{cases}
\end{align*}$$
- **Syntax**: Sintatical rules of the representations of sentences.
- **Semantics**: We use the calculate the semantical value of an expression, the "result", we can say.
- **Alphabet**:  Is the [[Sets|set]] of symbol from which the words of a language are built.
- **Language**: Set of words constructed from a certain alphabet.
We call $\Sigma^{*}$ the set of all possible strings constructed from an alphabet. A language $L$ is a [[Subsets|subset]] of $\Sigma^{*}$. $L \subseteq \Sigma^{*}$.
We can define $\Sigma^{*}$ recursively:
- Let $\Sigma$ be some alphabet.
- $\epsilon \in \Sigma^{*}$ ($\epsilon$ is the empty string)
- Every symbol $s \in \Sigma$ also belongs to $\Sigma^{*}$
- If $s \in \Sigma$ and $t \in \Sigma$, $s.t \in \Sigma^{*}$, where "$.$" is the concatenation operator.