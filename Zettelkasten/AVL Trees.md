---
tags: data-structures
---
**AVL** Trees are self-balancing *binary*-search-trees, that use internal, constant-time operations to remain balanced.

**Height of a node** is the height of the left subtree rooted at that node minus the height of the right subtree rooted at that node.

Here we assume the height of an empty subtree is -1.
The **balance factor** of a node is the difference between the heights of the left and right subtrees rooted at that node, in avl trees, a balance factor of $0,1$ or $-1$ is tolerated, that is.$|\rm{bf}| \le 1$. 
A node unbalanced at the left has a **positive height**, nodes unbalanced at the right have a positive height.

## Types of Rotation
$R-$Rotation: used when we insert at the left, on a left child of the unbalanced node. When we insert some value $k$ at that spot. when the recursion bubbles up and heights are updated, as soon as the following condition is matched: 
$$\begin{align*}
balance 
\end{align*}$$


$L$-Rotation: used when we insert at the right, on a right child of the unbalanced node.