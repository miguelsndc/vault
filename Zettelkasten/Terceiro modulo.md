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
## Homomorfismo
É um tipo de mapeamento entre estruturas, que é definido a partir de uma função do domínio de uma estrutura $A$ para o domínio de outra estrutura $B$.
Seja $L$ uma assinatura e sejam $A$ e $B$ $L$-estruturas. Seja $h$ uma função de $\f{dom}(A)$ em $\f{dom}(B)$: $(h: \f{dom}(A) \rightarrow \f{dom}(B))$. então $A$ é um **Homomorfismo da estrutura $A$ para $B$** se:
1. Para cada constante $c$ de $L$, $h(c^{A})=c^{B}$ *(Preserva as constantes)*
2. Para todo símbolo de relação $n$-ária de $R$ de $L$ e toda $n$-upla ($a_{1},\cdots,a_{n}$) de elementos de $A$, se $(a_{1},\cdots,a_{n})\in R^{A}$ então $(h(a_{1}),\cdots,h(a_{n}))\in R^{B}$. *(Preserva relacionamentos)*
3. Para todo símbolo de função $n$-ária de $g$ de $L$ e toda $n$-upla ($a_{1},\cdots,a_{n}$) de elementos de $A$, $h(g^{A}(a_{1},\cdots,a_{n}))= g^{B}(h(a_{1}),\cdots,h(a_{n}))$, *(Preserva as funções)*
___
## Imersão

Um tipo especial de **homomorfismo**, onde as propriedades são ligeiramente alteradas
1. Para cada constante $c$ de $L$, $h(c^{A})=c^{B}$ *(Permanece)*
2. Para todo símbolo de relação $n$-ária de $R$ de $L$ e toda $n$-upla ($a_{1},\cdots,a_{n}$) de elementos de $A$, **se e somente se** $(a_{1},\cdots,a_{n})\in R^{A}$ então $(h(a_{1}),\cdots,h(a_{n}))\in R^{B}$. *(Implica se transforma num se e somente se)*
3. Para todo símbolo de função $n$-ária de $g$ de $L$ e toda $n$-upla ($a_{1},\cdots,a_{n}$) de elementos de $A$, $h(g^{A}(a_{1},\cdots,a_{n}))= g^{B}(h(a_{1}),\cdots,h(a_{n}))$, *(Preserva as funções)*
4. $h$ deve ser **injetora** 

___
## Outros tipos de homomorfismos

- um **Isomorfismo** é uma imersão **sobrejetora**
- Homomorfismos $f: A\rightarrow A$ são chamados de **endomorfismos de $A$**
- Isomorfismos $f:A\rightarrow A$ são chamados de **automorfismos de $A$**.
___
## Subestrutura

> Como saber se uma estrutura $A$ é subestrutura de uma estrutura $B$ ?

Restrições:
- As duas tem que implementar a mesma assinatura

Nesse caso, se $A$ e $B$ forem simplesmente conjuntos, basta checar se todos os elementos de $A$ estão em $B$, $A \subseteq B$. 

Generalizando:

Sejam $A$ e $B$ duas $L$-estruturas. Dizemos que $A$ é uma subestrutura de $B$ $(A\subseteq B)$  se:
- $\f{dom}(A)\subseteq \f{dom}(B)$
- A função identidade de $\f{dom}(A)$ em $\f{dom}(B)$ é uma imersão.
___
## Termos

Termos são os argumentos dos predicados, um nome fresco pra parâmetros, porque aparentemente tudo tem que ser definido formalmente mesmo sendo estupidamente óbvio.

Seja $L$ uma assinatura. O conjunto de termos de $L$ é definido indutivamente como a seguir:
- Todo símbolo $c$ de constante de $L$ é um termo.
- Toda variável é um termo.
- Para todo símbolo de função n-ária $f$ de $L$, se $t_{1},\cdots,t_{n}$ forem termos, então $f(t_{1},\cdots,t_{n})$ é um termo.
- Nada mais é um termo

___
## Fórmulas atômicas

Os resultados das relações, os predicados aplicados aos termos btw. se não tem nenhum dos conectivos da lógica proposicional então é uma fórmula atômica.

Seja $L$ uma assinatura.
- Se $P$ é o símbolo da relação de $L$ com aridade $n$ e $t_{1},\cdots,t_{n}$ são termos de L, então $P(t_{1},\cdots,t_{n})$ é uma fórmula atômica.
- Se $t_{1}$ e $t_{2}$ são termos de $L$, então $t_{1}=t_{2}$ é uma fórmula atômica.
___
## Escopo de um Quantificador

Quantificadores são basicamente funções, o escopo de um quantificador é a expressão que ele recebe como parâmetro, isso é uma forma de limitar onde o quantificador atua, e calcular corretamente o valor das expressões.

$$\begin{align*}
\forall x(P(x) \implies \exists yR(x,y))
\end{align*}$$
O escopo de $\forall x$ é $P(x) \implies\exists yR(x,y)$.
___
## Variáveis lvi