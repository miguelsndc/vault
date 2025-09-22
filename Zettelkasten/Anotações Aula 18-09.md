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


> Se $A_{1}$ e $A_{2}$ são linguagens regulares, então $A_{1}\cup A_{2}$ também é regular.

**Prova**:
Assuma por hipótese que $A_{1}$ e $A_{2}$ são regulares, vamos demonstrar que $A_{1}\cup A_{2}$ também é regular. 
Da hipótese segue que existem $M_{1}$ e $M_{2}$ que reconhecem $A_{1}$ e $A_{2}$, tais que:
- $M_{1}= (Q_{1}, \Sigma, q_{0_{1}}, \delta_{1}, F_{1})$ 
- $M_{2}= (Q_{2}, \Sigma, q_{0_{2}}, \delta_{2}, F_{2})$
Vamos construir a partir de $M_{1}$ e $M_{2}$, um A.F que reconhece $A_{1} \cup A_{2}$, para este fim, definiremos um componente de $M_{3}$ por vez:
1. Estados ($Q_{3}$):
	Vamos definir os estados $Q_{3}$ de $M_{3}$ como sendo o produto cartesiano entre $Q_{1}$ e $Q_{2}$, ou seja, $Q_{3} = Q_{1} \times Q_{2}$.
2. Alfabeto $\Sigma$
	O alfabeto é igual pras duas então ele permanece inalterado.
3. Estado inicial $q_{0_{3}}$.
	 Vamos definir o estado inicial de $M_{3}$ como sendo o par ordenado $(q_{0_{1}}, q_{0_{2}})$, como definido no ponto $1$.
4. A função de transição $\delta_{3}$
	$\delta_{3}$ é definida da seguinte forma: para cada pair $(r_{1},r_{2}) \in Q_{3}$ e para cada símbolo do alfabeto, $a \in \Sigma$:
	$$\begin{align*}
\delta_{3}((r_{1},r_{2}), a) &= (\delta_{1}(r_{1}, a), \delta_{2}(r_{2}, a))
\end{align*}$$
	Portanto $\delta_{3}$ pega um estado de $M_{3}$, que é um par de estados composto por um estado de $M_{1}$ e outro de $M_{2}$, e retorna o próximo estado se decompondo em uma função para cada estado.o
5. O conjunto de estados de aceitação $F_{3}$, cujos membros podem ser *estados de aceitação de $M_{1}$ **ou** estados de aceitação de $M_{2}$*: $F_{3} =\{(r_{1},r_{2}) | r_{1}\in F_{1} \textrm{ or } r_{2} \in F_{2}\}$. Essa expressão é equivalente a $F_{3} = (F_{1}\times Q_{2}) \cup (Q_{1}\times F_{2})$ . Note que isso é diferente de $F_{3}= F_{1}\times F_{2}$, isso nos daria a **interseção** de $F_{1}$ e $F_{2}$, e neste caso, nos daria a linguagem que é a interseção, não união, com isso, a interseção de linguagens regulares também está definida. 

**Teorema**: complemento de uma linguagem regular $L$ também é regular.

*Se $L$ é uma linguagem regular, então o complemento $L'$ também é regular*

**Prova**:
Assuma por hipótese que $L$ é regular, vamos demonstrar que $L'$ também é regular. Da hipótese existe um $M = \{Q, \Sigma, q_{0}, \delta, F\}$ um autômato finito que reconhece a linguagem $L$, vamos utilizar $M$ para construir outro A.F $M' = \{Q', \Sigma, q_{0}', \delta', F' \}$ que reconhece $L'$.
Perceba que $M'$ deve reconhecer tudo que $L$ não reconhece, e não reconhecer tudo que $L$ reconhece, ou seja, o conjunto dos estados de aceitação de $M'$  deve ser o complemento do de $M$. então temos que:
1. $Q = Q'$
2. $\Sigma$ continua igual.
3. $q_{0}=q_{0}'$
4. $\delta = \delta_{'}$
5. Apenas $F' = (Q - F)$.
Agora o A.F construído $M'$ reconhece o complemento da linguagem $L$, como descrito acima.


##### Autômatos finitos não determinísticos

