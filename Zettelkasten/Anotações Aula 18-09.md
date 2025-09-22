##### Linguagens Regulares

Uma linguagem $A$ é dada como **regular** se existe um autômato finito que reconhece essa linguagem.

##### Operações Regulares

**Teorema**: a classe das linguagens regulares é fechada sob:
1. União $A \cup B = \{x | x \in A \textrm{ or } x \in B \}$    
2. Concatenação $A \circ B = \{xy|x \in A \textrm{ and } y \in B\}$  
3. Interseção $A \cap B = \{x | x \in A \textrm{ and } x \in B\}$
4. Estrela $A^{*} = \{x_{1}x_{2}\cdots x_{k} | k \ge 0 \text{ and each } x_{i}\in A\}$ 
5. Complemento $\bar{A} = \{x | x \in A^{*} \text{ and } x \notin A\}$
