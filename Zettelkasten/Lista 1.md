Questão 4

> [!faq]
> Use o lema do bombeamento para mostrar que as liguagens a seguir não são regulares.
> - $A_{1} = \{ 0^{n}1^{n}2^{n} | n \geq 1 \}$


$A_{1} = \{ 0^{n}1^{n}2^{n} | n \geq 1 \}$

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




