
> [!faq] Questão 4
> Use o lema do bombeamento para mostrar que as liguagens a seguir não são regulares.
> - $A_{1} = \{ 0^{n}1^{n}2^{n} | n \geq 1 \}$
> - $A_{2} = \{ www | w \in \{a,b\}^{*} \}$


- $A_{1} = \{ 0^{n}1^{n}2^{n} | n \geq 1 \}$

Suponha por contradição que $A_{1}$ é regular. Então, pelo Lema do Bombeamento, existe um comprimento de bombeamento $p \geq 1$. 

Seja a palavra $w = 0^{p}1^{p}2^{p}$
- Sabemos que $w \in L$, pois ela tem exatamento $p$ símbolos $0$ seguidos por $p$ símbolos $1$ e $p$ símbolos $2$.
- O comprimento total da palavra é $|w| = 3p$. Com $p \geq 1$, temos que $|w| \geq p$, o que satisfaz a condição inicial do lema para a palavra ser elegível ao bombeamento.

Pelo lema, sabemos que $w$ pode ser dividida em três partes, $w = xyz$ que obrigatoriamente satisfazem as seguintes condições:
1. $|y| > 0$ (a parte $y$ não pode ser vazia).
2. $|xy| \leq p$ (as partes $x$ e $y$ juntas têm tamanho máximo $p$).
3. Para todo $i \geq 0$ $xy^{i}z \in L$.

Observe a condição $2$ ($|xy| \leq p$). A nossa palavra escolha $w = 0^{p}1^{p}2^{p}$ começa com exatamente $p$ zeros. Como $x$ e $y$ juntas ocupam no máximo os primeiros $p$ caracteres da palavra, isso garante que a subcadeia $xy$ é composta **exclusivamente** por zeros. Consequentemente, a parte $y$ (que é o trecho que será bombeado), é formada apenas por zeros. Vamos dizer que $y$ contém $k$ zeros, onde $k > 0$ (Condição 1).

Vamos testar a Condição 3 escolhendo $i = 2$. Isso significa que vamos bombear a palavra uma vez, criando a nova cadeia $xy^{2}z$ ou $xyyz$.
- Ao fazer isso, adicionamos mais uma cópia de $y$ à palavra.
- Como $y$ é composto por $k$ zeros, a nova palavra terá $p + k$ zeros.
- A quantidade de símbolos $1$ e símbolos $2$ em $z$ não foi alterada, permanecendo exatamente $p$
- Como $k > 0$, o número de zeros ($p + k$) agora é estritamente maior que o número de símbolos $1$ e $2$.

A nova palavra $xy^{2}z$ tem mais símbolos $0$ do que símbolos $1$ e $2$, logo, não possui o formato $0^{n}1^{n}2^{n}$. Portanto, $xy^{2}z \notin L$. Isso viola a Condição 3 do Lema do Bombeamento, gerando uma contradição com nossa suposição inicial. Sendo assim, a linguagem $L$ não é regular.
___
- $A_{2} = \{ www | w \in \{a,b\}^{*} \}$

Suponha por contradição que $A_{2}$ é regular. Então, pelo Lema do Bombeamento, existe um comprimento de bombeamento $p \geq 1$. 

Seja a palavra $s = a^{p}b a^{p}b a^{p}b$.
- Sabemos que $s \in L$, pois ela é formada pela repetição de três cadeias idênticas $w = a^{p} b$.
- O comprimento total da palavra é $|s| = 3p + 3$. Com $p \geq 1$, temos que $|s| \geq p$, o que satisfaz a condição inicial do lema para a palavra ser elegível ao bombeamento.

Pelo lema, sabemos que $s$ pode ser dividida em três partes, $s = xyz$ que obrigatoriamente satisfazem as seguintes condições:
1. $|y| > 0$ (a parte $y$ não pode ser vazia).
2. $|xy| \leq p$ (as partes $x$ e $y$ juntas têm tamanho máximo $p$).
3. Para todo $i \geq 0$ $xy^{i}z \in L$.

Observe a condição $2$ ($|xy| \leq p$). A nossa palavra escolha $w = a^{p}b a^{p}b a^{p}b$ começa com exatamente $p$ símbolos $a$. Como $x$ e $y$ juntas ocupam no máximo os primeiros $p$ caracteres da palavra, isso garante que a subcadeia $xy$ é composta **exclusivamente** por símbolos $a$. Consequentemente, a parte $y$ (que é o trecho que será bombeado), é formada apenas por símbolos $a$. Vamos dizer que $y$ contém $k$ símbolos $a$, onde $k > 0$ (Condição 1).

Vamos testar a Condição 3 escolhendo $i = 2$. Isso significa que vamos bombear a palavra uma vez, criando a nova cadeia $xy^{2}z$ ou $xyyz$.
- Ao fazer isso, adicionamos mais uma cópia de $y$ à palavra.
- Como $y$ é composto por $k$ símbolos $a$, a nova palavra terá $p + k$ símbolos $a$.
- A quantidade de símbolos no restante da palavra (a parte z) não foi alterada, de modo que a string nova fica com o formato $a^{p+k}b a^{p}b a^{p}b$
- Para que essa palavra continuasse pertencendo a $A_{2}$, ela precisaria ser perfeitamente divisível em três partes idênticas. Como a palavra inteira possui apenas três simbolos $b$, a única forma de dividí-la em três partes iguais seria quebrar a string após cada símbolo $b$. No entanto, isso nos daria as três partes: $a^{p+k}b$, $a^{p}b$ e $a^{p}b$.

Como $k> 0$, o primeiro bloco $a^{p+k}b$ agora é estritamente maior e diferente dos outros dias. A nova palavra $xyyz$ não pode ser dividida no formato $www$. Portanto $xyyz \notin A_{2}$. Isso viola a Condição 3 do Lema do Bombeamento, gerando uma contradição com nossa suposição inicial. Sendo assim, a linguagem $A_{2}$​ não é regular.

___

> [!faq] Questão 5
> Para qualquer cadeia $w = w_{1}w_{2}\cdots w_{n}$ o reverso de $w$, escrito $w^{R}$ é a cadeia $w$ na ordem reversa $w = w_{n} \cdots w_{2}w_{1}$. Para qualquer linguagem $A$, seja $A_{R} = \{ w^{R}| w \in A \}$  Mostre que se $A$ é regular, então $A^{R}$ é regular.

Se a linguagem $A$ é regular, então existe um autômato finito determinístico que a reconhece. Seja $M = (Q,\Sigma,\delta,q_{0},F)$, esse autômato.  

Vamos construir um autômato finito não-determinístico para reconhecer $A^{R}$. Seja $M^{R} = (Q^{R},\Sigma,\delta^{R},q_{novo},F^{R})$ esse autômato, onde:

1. $Q^{R} = Q \cup \{q_{novo}\}$.
2. $q_{novo}$ é o novo estado inicial.
3. $F^{R}= \{q_{0}\}$.
4. A nova função $\delta^{R}$ é definida da seguinte forma:
	- Para cada transição original $\delta (q, a) = p$ em $M$, criamos a transição reversa $q \in \delta^{R}(p, a)$ em $M^{R}$.
	- Como o autômato original podia ter vários estados finais em $F$, o novo autômato precisa começar a leitura a partir deles. Adicionamos $\delta^{R}(q_{novo}, \epsilon) = F$. Ou seja, do novo estado inicial transicionamos espontaneamente para qualquer um dos estados finais de $M$.

Como construímos um AFN que reconhece $A^{R}$, e todo AFN possui um AFD equivalente, $A^{R}$ é regular.

___

> [!faq] Questão 6
> Seja $C_{n}= \{ x | \text{x é um número binário múltiplo de n} \}$  Mostre que para cada $n\geq 1$ a linguagem $C_{n}$ é regular.

Para que $C_{n}$ seja regular, deve existir um autômato finito determinístico que a reconhece. Seja $M = (Q, \Sigma,\delta,q_{inicial},F)$ um AFD onde:

1. $Q = \{q_{0},q_{1},\cdots q_{n-1}\}$ onde $q_{i}$ representa a classe de congruência $[i]_{n}$.  
2. $\Sigma = \{0, 1\}$.
3. $\delta(q_{i}, b) = q_{(2i + b) \mod n}$. 
4. $q_{inicial} = q_{0}$.
5. $F = \{q_{0}\}$.

A linguagem $C_n$​ é regular porque construímos um AFD $M$ válido que a reconhece. O modelo possui exatamente $n$ estados cobrindo todas as classes de congruência possíveis, e a transição $\delta(q_{i}​,b)=q_{(2i+b) \mod n}​$ garante que rastreamos corretamente a classe que contém o valor formado conforme os bits são lidos da esquerda pra direita.

___

> [!faq] Questão 7
> Seja $\Sigma ={0,1,+,=}$ e $SOMA = \{x = y+z | \text{ x,y e z são inteiros binários e x é a soma de y e z}\}$. Mostre que $SOMA$ não é regular.


