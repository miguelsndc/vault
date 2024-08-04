---
tags: logic
---
*1)*  
- $a)$ É um conjunto $Y$ tal que $Y$ contém $X$ e é fechado sobre as funções de $F$.
- $b)$ É o menor conjunto $Y$ tal que $Y$ contém $X$ e é fechado sobre as funções de $F$.
- $c)$ É um conjunto indutivo $Y$ sobre $X$ e $F$ tal que:
	- Os conjuntos imagem das funções de $Y$ são disjuntos.
	- As funções de $Y$ são injetoras.
	- A base não pode ser gerada pelas funções de $Y$.

$2)$ Um conjunto ser livremente gerado garante que não há ambiguidade na geração das expressões legítimas do mesmo, assim podendo reduzir as expressões aos átomos e calcular os valores das expressões sem confusões, garantindo que cada resultado é gerado apenas de uma única forma.

$3)$ 
- Como existem infinitos conjuntos indutivos sobre $X$ e $F$, basta calcular a interseção de todos os conjuntos até o infinito, $\bigcap_{i=1}^{\infty}X_{i} = X^{+}$ será o fecho indutivo sobre $X$ e $F$. 
- Podemos definir o fecho indutivo como:
	- Base: $X_{0}= X \cup \{f(w_1,\cdots,w_{k})|$ aridade de $f=k$ e $w_{1},w_{2},\cdots,w_{k}\in X \}$  
	- $X_{i+1}= X_{i} \cup \{f(w_1,\cdots,w_{k})|$ aridade de $f=k$ e $w_{1},w_{2},\cdots,w_{k}\in X_{i} \}$ 
	- Portanto o fecho indutivo é $\bigcup_{i=0}^{\infty}X_{i} =X_{+}$  
Para mostrarque $X^{+}=X_{+}$ precisamos demonstrar a igualdade entre os dois conjuntos, isto é $X^{+}\subseteq X_{+}$ e $X_{+}\subseteq X^{+}$.

- $(i)$ $X_{+}\subseteq X^{+}$ :
	- Para demonstrar que $X_{+}\subseteq X^{+}$, basta mostrar que $X_{+}$ é um conjunto indutivo sobre $X$ e $F$, por conta da definição de $X^{+}$ como interseção de todos os conjuntos indutivos sobre $X$ e $F$.
	- $X_{+}$ contém $X$ pela definição, pois $X= X_{0}$ e $X_$
	- 