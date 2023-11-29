---
tags: combinatorics
---
The rule of sum a counting approach that let us identify the total possible choices for a procedure that combines two or more events where these events cannot happen at the same time.

>[!info] Intuitive Definition
>If a task can be done in either one of $n_{1}$ ways **or** one of $n_{2}$ ways, where the two sets of ways are **[[Disjoint Set|disjoint]]** then there are $n_{1}+n_{2}$ ways to complete the task. 

But the sum rule can be phrased in terms of [[Sets]]:

>[!tip] Definition in Terms of Sets
>$\mid A \cup B \mid = \mid A \mid + \mid B \mid$ as long as $A$ and $B$ are [[Disjoint Set|disjoint]]. Or, more generally:
>$\mid A_{1} \cup A_{2}\cup \cdots \cup A_{m} \mid = \mid A_{1} \mid + \mid A_{2}\mid + \cdots + \mid A_{m} \mid$ when $\forall i \forall j \mid A_{i}\bigcap A_{j}=\emptyset$
