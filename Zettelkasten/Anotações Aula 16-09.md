**Reconhecedores de linguagem**

Determina se uma palavra de um alfabeto pertence ou não a linguagem sobre o alfabeto, com um algoritmo definido, lê símbolos da esquerda para a direita, símbolo a símbolo, sem poder retroceder.

É uma máquina de estados que pode ser modelada como um automaton, um grafo direcionado onde vértices são estados e arestas são transições de estado para estado, a cada símbolo que se lê se define uma aresta no grafo.

Um autômato **reconhece** apenas uma linguagem.

Existe uma função de transição e um conjunto de estados para o autômato:

$Q = \{q_1 , q_2, , \cdots, q_n\}$
$\delta: Q \times \Sigma \rightarrow Q$

onde as transações são definidas uma a uma, pelo menos nesse exemplo:

$\delta(q_i, x) = q_{i +1}$

e assim por diante

Vértices onde a leitura termina e a palavra é aceita, são definidos com dois círculos, ou seja, existe um subconjunto $F \subseteq Q$ que são chamados **estados de aceitação**.

A linguagem do reconhecer é o conjunto de palavras que $M$ aceita, sendo $M$ a *máquina de estados*, o autômato.

**Autômato Finito**

Um autômato é especificado por seus componentes 
- Um conjunto de estados 
- Um estado inicial
- O alfabeto 
- A função de transição 
- Conjunto de Estados de aceitação 
O autômato é uma 5-upla formada pelos componentes acima.
O autômato é dito **finito** pois seu conjunto de estados é finito.

Um autômato *M* aceita *W* se existe uma sequência de estados de M onde o primeiro estado é o estado inicial, o estado final é um Estado de aceitação, e $\delta(s_i, w_i) = s_{i + 1}$, para todo $i \lt n$ .

**Como provar que um autômato $M$ reconhece uma linguagem $L$**

Para toda palavra $w \in \Sigma^*$ $M$ aceita $W$ se e somente se $W \in L$.

Será utilizado o princípio da indução.






