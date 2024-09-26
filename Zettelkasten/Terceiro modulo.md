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
## Variáveis livres e ligadas

Uma ocorrência de uma varíavel em uma fórmula é ligada se e somente se ela está no escopo de um quantificador aplicado a ela. Ou ela é a ocorrência do quantificador. Uma ocorrência de uma variável numa fórmula é livre se e somente se essa ocorrência não for ligada.

Uma variável é livre numa fórmula se pelo menos uma ocorrência dela é livre na fórmula. Uma variável é ligada se pelo menos uma ocorrência dela é ligada.

Uma variável, como se pode ver, pode ser livre e ligada, ambas definições não são mutuamente exclusivas, se a variável não aparece na declaração de um quantificador ela é livre, se aparece na de outro quantificador, é ligada.
___
## Fórmulas bem formadas

- Um átomo (fórmula atômica) é uma fórmula;
- se $F$ e $G$ são fórmulas, então $\neg(F)$, $(F \lor G)$, $(F \land G)$, $(F \implies G)$ e $(F \iff G)$ são fórmulas;
- Se $F$ é uma fórmula e $x$ é uma variável livre em $F$, então $\forall x F$ e $\exists x F$ são fórmulas;
- Fórmulas são geradas apenas por um finito número de aplicações das regras acima.
___
## Sentenças
Sentenças são fórmulas sem variáveis livres. Dessa forma, uma sentença atômica é uma fórmula atômica sem variável.
Exemplos de sentenças:
- $\forall x P(x)$, $\exists y M(y)$
Sentenças atômicas:
- $M(a)$, $P(b)$.
___
## Sentenças Atômicas

Sentença é uma fórmula sem variável livre, e se é atômica, não tem variável.

Seja $L$ uma assinatura e $\phi$ uma sentença atômica de $L$. O significado de $\phi$ segundo uma interpretação de $L$ numa estrutura $A$ de assinatura $L$ é determinado pelo resultado da interpretação sobre os termos de $\phi$ e sobre o símbolo de relação $\phi$.

Basicamente nada significa porra nenhuma, tudo depende da interpretação dos termos e das relações, estamos no mundo da fantasia

![[Pasted image 20240923121652.png]]
___
## Modelo de uma sentença atômica

Seja $L$ uma assinatura e $A$ uma $L$-estrutura. Dizemos que $A$ é um modelo de $\phi$ sob uma determinada interpretação de $L$ em $A$ se $\phi^{A}$ for verdadeira.
## Contra-Modelo de uma sentença atômica

Seja $L$ uma assinatura e $A$ uma $L$-estrutura. Dizemos que $A$ é um contra-modelo de $\phi$ sob uma determinada interpretação de $L$ em $A$ se $\phi^{A}$ for falsa.
___
## Sentenças e estruturas

Veremos como passar de uma estrutura para um conjunto de sentenças que a descrevem. E como passar de um conjunto de sentenças para uma estrutura que satisfaz esse conjunto.

1. De estruturas para sentenças;
2. De sentenças para estruturas.

## Diagrama positivo (Estruturas $\rightarrow$ Sentenças)

Seja $A$ uma $L$-estrutura. O conjunto de todas senteças atômicas de $L$ que são verdadeiras sob uma determinada interpretação em $A$, (ou seja, a descrição lógica de $A$) é chamado de diagrama positivo de $A$.

O processo de construção é dado por:

1. Para todo símbolo de relação $n$-ária $R$ de $L$, inclua uma sentença atômica da forma $R(t_{1},\cdots,t_n)$ se os elementos $(t_{1}^{A}, \cdots, t_{n}^{A}) \in R^{A}$.
2. Para todo símbolo de função $n$-ária $f$ de $L$ inclua uma sentença atômica da forma $f(t_{1},\cdots,t_{n})=t_{n+1}$ se, $f^{A}(t_{1}^{A}, \cdots, t_{n}^{A})= t^{A}_{n+1}$ na estrutura $A$ onde $t^{A}_{1}, \cdots, t^{A}_{n}$ são representações dos elementos de $A$.

## Extensão de uma estrutura

Seja $A$ uma $L$-estrutura. Quando desejamos produzir o diagrama positivo de $A$ e $A$ tem elementos "sem nome", definimos uma **extensão** de $A$, chamada $A'$ que admite esses "sem nome", como novos elementos destacados

Isso significa dizer que a assinatura $A'$ é $L' = L \cup \{c_{1},\cdots,c_{n}\}$.

Onde $c_{i}$ é um símbolo de constante para representar o elemento $a_{i}$. Às vezes abreviamos $L \cup \{c_{1},\cdots, c_{n}\}$ como $L(\bar{c})$.

## Diagrama positivo
Aparentemente o diagrama positivo é só aplicar as relações / funções algumas vezes nas constantes, quantas vezes ? quantas seu coração mandar, mas pelo menos umas duas, e faz isso pra cada relação/função.
Nas funções você estabelece igualdade entre as constantes e algumas funções algumas vezes também, complicação da porra pra dizer isso.
![[Pasted image 20240923143021.png]]
tipo assim tlgd

## Modelo Canônico

é assim q a gente pega um conjunto de sentenças e transforma numa estrutura

![[Pasted image 20240923143738.png]]
**Pra achar o domínio**:
Olha as constantes:
- $k$ e $t$ 
Olha as funções e todas as possíveis permutações de constantes nessas funções:
- Nesse caso tem $g$ e $p$ $g$ com $1$ parametro e $p$ com $2$, então a gnt ta atrás dos valores de:
	- $g(t),g(k),p(k,k),p(k,t),p(t,k),p(t,t)$.
Aí a gente vai buscar as classes de equivalencia das constantes, caso tenha alguma sentença aí que nao dê pra colocar em nenhuma classe de equivalencia a gente abre outra, tem bronca nao:
$$\begin{align*}
k^{*} &= \{k, g(t), g(k),p(k,t),  \}\\
t^{*}&= \{t, p(k,k) \}\\
p(t,k)^{*} &= \{ p(t,k), p(t,t) \}
\end{align*}$$
Aí o $\f{dom}(A) = \{k^{*}, t^{*}, p(t,k)^{*}\}$.

**Destaques**: simplesmente as classes de equivalencia das constantes: $\{k^{*},t^{*}\}$.
**Relacionamentos**: $\{X^{A}(),Y^{A}(,)\}$.
Tem que ver quem que está em cada relacionamento, tipo, achar os pares:
$$\begin{align*}
X &=\{k^{*}\}\\
Y &=\{(k^{*}, t^{*}), (k^{*},k^{*})\}
\end{align*}$$
Só olhar as sentenças e substituir os valores pelas classes de equivalência e jogar esse par dentro do conjunto.
**Funções**: $\{g^{A}(), p^{A}(,)\}$, só olhar as funções.
## Retomando SAT
ai meus ovo, o sat denovo nao

Dado um conjunto $C$ de sentenças da lógica de primeira ordem. Pergunta-se, $C$ é satisfatível ?

> C tem um modelo ?

Se $C$ for um conjunto de sentenças atômicas é só usar o algoritmo dali de cima pra achar o modelo **canônico**, se não for amigo deu merda federal kkkkkkkk. Lembrando que modelos são uma estrutura onde as sentenças interpretadas naquele modelo são verdadeiras, eu chuto que pra ser satisfatível o modelo tem que ser true pra todas as sentenças do conjunto.

## Substituição de variáveis por termos

Aparentemente trocar as letras ajuda de alguma forma, então a sintaxe pra isso, numa FBF *(Fórmula bem formada)* é: $P(x)[a/x]$, no predicado $P(x)$ sai o $x$ e entra o $a$ no lugar, daí aquela mesma história da definição recursiva pra todos os conectivos:
- Se $\phi$ é atômica temos $\phi[t/x]$. É a fórmula resultante da remoção de todas as ocorrências de $x$ e a colocação do termo $t$ nos seus lugares.
- Se $\phi$ é da forma $\neg \phi:(\neg\phi)[t/x]=\neg(\phi[t/x])$. 
- Se $\phi$ é da forma $(\delta \land \rho):(\delta\land\rho)[t/x]=(\delta[t/x]\land \rho[t/x]);$  
- Se $\phi$ é da forma $(\delta \lor \rho):(\delta\lor\rho)[t/x]=(\delta[t/x]\lor \rho[t/x]);$  
- Se $\phi$ é da forma $(\delta \implies \rho):(\delta\implies\rho)[t/x]=(\delta[t/x]\implies \rho[t/x]);$  
**Apenas substituem-se variáveis, constantes não.**
não vou escrever isso nem fudendo
![[Pasted image 20240923150852.png]]
Só se aplica substituição em variáveis livres, substituição em variáveis ligadas é inócua.

Substituções que alteram o significado da fórmula são consideradas inválidas, não se pode substituir uma variável livre por uma variável ligada, como no exempo:

$$\begin{align*}
(\forall x)(\forall y)(P(x,y) \implies R(z))[y/z]
\end{align*}$$
Não se pode substituir o $z$ pelo $y$, pois z ocorria livre, portanto não pode ser substituída por uma variável que ocorre ligada.

**Não se pode mudar o status da variável.**
___
## Substituições aplicadas a termos

Pode-se aplicar substituição somente à termos também, usa-se a mesma notação e as mesmas regras se aplicam $s[t/x]$ substituição da variável $x$ pelo termo $t$ so termo $s$.

## Valor-verdade de uma sentença

Seja $L$ uma assinatura, $A$ uma $L$-estrutura e $.^{A}$ uma interpretação dos símbolos de $L$ na $L$-estrutura. O valor-verdade de uma sentença $\phi$ de $L$ é definida indutivamente da seguinte forma:

1. Se $\phi$ é atômica:
	1. é da forma $R(t_{1},\cdots,t_{n})$:
			$\phi^{A}$ é verdade se e somente se $(t_{1}^{A}, \cdots, t_{n}^{A}) \in R^{A}$.
	2. é da forma $t1=t2$
			$\phi^{A}$ é verdade se e somente se $$