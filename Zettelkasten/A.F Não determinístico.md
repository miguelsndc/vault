---
tags: theory
aliases: NFA
---

Autômatos determinísticos são chamados assim pois possuem apenas um ramo de computação, ou seja, para cada estado existe apenas uma transição que pode ser feita para o próximo estado para cada elemento do alfabeto. Em NFA (Non-deterministic finite automata) existem várias transições. O nome não-determinístico jaz nessa noção de que para cada estado podem haver várias formas de transicionar para um próximo estado.

Um NFA computa a partir de uma "complete-search",  para cada transição que possivelmente gera uma nova branch, a máquina se divide em duas para cada transição e continua a computar a partir do ponto que parou, dizemos que um NFA **aceita** uma palavra $w$ se existe pelo menos um caminho nas transições que leve para um estado de aceitação, caso contrário, o NFA rejeita $w$. 

Em NFA também podem existir transições vazias, isto é, onde o valor da transição é o símbolo da cadeia vazia, que pode não pertencer ao alfabeto, quando isto acontece, a máquina se divide em duas, uma continua no estado atual e uma cópia da máquina atual vai para o estado onde a transição vazia ocorreu, e continua a leitura do próximo caractere.

A transição vazia é útil para testar várias possibilidades sem necessariamente precisar ler um caractere da palavra.i

#### Definição Formal 

A definição de um autômato finito não determinístico ou NFA é parecida com a dos determinísticos, com uma peculiaridade, a **função de transição**, dado que existem múltiplas escolhas de transição para um estado, precisamos definir isso na função de transição, então introduzimos notação:

- $P(Q)$ é chamado [[Power Set]] ou conjunto das partes de $Q$, é a coleção de todos os subconjuntos de $Q$.
- Quando escrevermos $\Sigma_{\epsilon}$ entenda como $\Sigma \cup \{\epsilon\}$. Vamos precisar para incluir as transições vazias.

Então escrevemos $\delta: Q \times \Sigma_{\epsilon} \rightarrow P(Q)$.

> [!tip] Definição
>Um **autômato finito não-determinístico** é uma $5$-upla $(Q,\Sigma, \delta, q_0 , F)$,
>onde:
>- $Q$ é um conjunto finito de estados
>- $\Sigma$ é um alfabeto finito.
>- $\delta: Q \times \Sigma_{\epsilon} \rightarrow P(Q)$
>- $q_0 \in Q$ é o estado inicial e
>- $F \subseteq Q$ é o conjunto de estados de aceitação.

A definição de **computação** para um NFA também é similar ao de um DFA, perceba: Seja $N = (Q,\Sigma, \delta, q_0 , F)$ um NFA e $w$ uma palavra sobre o alfabeto $\Sigma$, dizemos que $N$ **aceita** $w$ se podemos escrever $w$ como $w = y_1 y_2 \cdots y_m$, onde cada $y_i$ é um membro de $\Sigma_{\epsilon}$ e a sequência de estados $r_0, r_1, \cdots, r_m$ existe com as condições:

- $r_0 = q_0$
- $r_{i + 1} \in \delta(r_i, y_{i + 1}$) para $i = 0, 1, \cdots, m - 1$ e
- $r_m \in F$ 


