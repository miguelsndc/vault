Proposições agora são funções que recebem parâmetros, houve a introdução dos quantificadores, existencial e universal.

Estruturas são os simbolos, é necessário representar os objetos, os predicados e as constantes.

Formalmente, trata-se de um conjunto ampliado $A$ com:
- Um conjunto de elementos chamado de "domínio" de $A$ (denotado por $\f{dom}(A)$ ou "universo" de $A$. É o conjunto de objetos
- Um conjunto de relações sobre $\f{dom}(A)$, cada uma com sua aridade
- Uma coleção de elementos de $\f{dom}(A)$, que são considerados destacados
- Um conjunto de funções sobre $\f{dom}(A)$, cada uma com sua aridade
**Qualquer um dos quatro conjuntos pode ser vazio**.
___
## Assinatura
Um conjunto que reúne as seguintes informações:
- Os elementos destacados
- As relações e suas respectivas aridades
- As funções e suas respectivas aridades
Este conjunto é dito a assinatura de uma estrutura.
A assinatura serve como se fosse uma interface de uma estrutura, caso duas (ou mais) estruturas tenham a seguinte assinatura:
- *2 Destaques: $a$ e $b$*;
- *$1$ relação binária: $R(\_,\_)$ e $1$ relação unária $S(\_)$* 
- *$1$ função binária: $g(\_,\_)$ e $1$ função unária $f(\_)$* 
 As estruturas obedecendo essa assinatura podem ser facilmente trocadas umas pelas outras, oferecendo diferentes comportamentos.

Estrutura $A,B$:
O valor de $a^{A}= 1$ e $b^{A}=3$ e $a^{B}=-2$ e $b^{B}=4$, onde a potência indica qual estrutura é trabalhada.
___
## Subestrutura
