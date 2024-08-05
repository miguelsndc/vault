---
tags: logic, semantics
---
A *Valuation* is a [[Functions|function]] $v:X \rightarrow Z$ such that there exists a *extension* $\hat{v}: X_{+}\rightarrow Z$ where $X$ is the [[Definitions of Logic|basis]] and $X_{+}$ the [[Inductive Sets and Closures|inductive closure]] of $X$ and $F$, such that:
- $\hat{v}(e_{1})=v(e_{1})$ if $e_{1}$ is atomic.
- $\hat{v}((e_{1}\land e_{2})) = \textrm{AND}(\hat{v}(e_{1}), \hat{v}(e_{2}))$    
- $\hat{v}((e_{1}\lor e_{2})) = \textrm{OR}(\hat{v}(e_{1}), \hat{v}(e_{2}))$    
- $\hat{v}((e_{1}\implies e_{2})) = \textrm{IMPLIES}(\hat{v}(e_{1}), \hat{v}(e_{2}))$    
- $\hat{v}((\neg e_{1})) = \textrm{NEG}(\hat{v}(e_{1}))$     
The $v$ function assignes values to atomic expressions, while the $\hat{v}$, $v$'s extension, is defined recursively such that the expressions are broken down until we reach the atomic expressions, then we evaluate with $v$ and backtrack, This can be done with $PROP$, since it's a [[Freely Generated Sets|freely generated set]], and using the [[Recursive Functions over PROP]] we can use such values. 

For example, the value of $((P \implies R) \lor (\neg Q))$ is:
$$\begin{align*}
\begin{cases}
v(P)=1\\
v(R)=1\\
v(Q)=0\\
\end{cases}\\
\\

\hat{v}(((P \implies R) \lor (\neg Q)))&= \textrm{OR}(\hat{v}((P \implies R)), \hat{v}((\neg Q)))\\
&= \textrm{OR}(\textrm{IMPLIES}(\hat{v}(P), \hat{v}(R)),\textrm{NEG}(\hat{v}(Q)))\\
&=\textrm{OR}(\textrm{IMPLIES}(v(P), v(R)),\textrm{NEG}(v(Q)))\\
&=\textrm{OR}(\textrm{IMPLIES}(1, 1),\textrm{NEG}(0))
\end{align*}$$
