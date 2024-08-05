---
tags: logic, semantics
---
A *Valuation* is a [[Functions|function]] $v:X \rightarrow Z$ such that there exists a *extension* $\hat{v}: X_{+}\rightarrow Z$ where $X$ is the [[Definitions of Logic|basis]] and $X_{+}$ the [[Inductive Sets and Closures|inductive closure]] of $X$ and $F$, such that:
- $\hat{v}(e_{1})=v(e_{1})$ if $e_{1}$ is atomic.
- $\hat{v}((e_{1}+e_{2})) = sum(\hat{v}(e_{1}), \hat{v}(e_{2}))$    
- $\hat{v}((e_{1}*e_{2})) = mul(\hat{v}(e_{1}), \hat{v}(e_{2}))$    

