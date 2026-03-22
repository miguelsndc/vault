Questão 4

> [!faq]
> Use o lema do bombeamento para mostrar que as liguagens a seguir não são regulares.
> - $A_{1} = \{ 0^{n}1^{n}2^{n} | n \geq 1 \}$


$A_{1} = \{ 0^{n}1^{n}2^{n} | n \geq 1 \}$

Suponha por contradição que $A_{1}$ é regular. Então, pelo Lema do Bombeamento, existe um comprimento de bombeamento $p \geq 1$. 

Seja a palavra $w = 0^{p}1^{p}2^{p}$
- Sabemos que $w \in L$, pois ela tem exatamento $p$ símbolos $0$ seguidos por $p$ símbolos $1$ e $p$ símbolos $2$.
- O comprimento total da palavra é $|w| = 3p$. Com $p \geq 1$, temos que $|w| \geq p$, o que satisfaz a condição inicial do lema para a palavra ser elegível ao bombeamento.

Pelo 

