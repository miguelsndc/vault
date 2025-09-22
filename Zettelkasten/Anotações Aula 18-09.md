##### Linguagens Regulares

Uma linguagem $A$ é dada como **regular** se existe um autômato finito que reconhece essa linguagem.

##### Operações Regulares

**Teorema**: a classe das linguagens regulares é fechada sob:
1. União $A \cup B = \{x | x \in A \textrm{ or } x \in B \}$    
2. Concatenação $A \circ B = \{xy|x \in A \textrm{ and } y \in B\}$  
3. Interseção $A \cap B = \{x | x \in A \textrm{ and } x \in B\}$
4. Estrela $A^{*} = \{x_{1}x_{2}\cdots x_{k} | k \ge 0 \text{ and each } x_{i}\in A\}$ 
5. Complemento $\bar{A} = \{x | x \in A^{*} \text{ and } x \notin A\}$


Seja $M_1$ um A.F que reconhece $A_{1}$, onde $M_{1} =\{Q_{1},\Sigma, \delta_{1}, q_{1}, F_{1}\}$ e 
    $M_{2}$ um A.F que reconhece $A_{2}$ onde $M_{2}  =\{Q_{2},\Sigma, \delta_{2}, q_{2}, F_{2}\}$

*Vamos construir um A.F $M_{3}$ que reconhece $A_{1}\cup A_{2}$ onde $M_{3} =\{Q_{3},\Sigma, \delta_{3}, q_{3}, F_{3}\}$, ou seja, que linguagens regulares são fechadas sob a operação de união.*
*Para demonstrar que $M_{3}$ é de fato um A.F e que reconhece $A_{1} \cup A_{2}$, lembrando a definição de A.F, precisamos definir cada componente de $M_{3}$.*

Sejam $A_{1}$ e $A_{2}$ linguagens regulares,


