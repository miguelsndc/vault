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

- $(i)$ $X^{+}\subseteq X_{+}$ :
	- Para demonstrar que $X^{+}\subseteq X_{+}$, basta mostrar que $X_{+}$ é um conjunto indutivo sobre $X$ e $F$, por conta da definição de $X^{+}$ como interseção de todos os conjuntos indutivos sobre $X$ e $F$.
	- $X_{+}$ contém $X$ pela definição, pois $X= X_{0}$ e $X_{+}\subseteq X_{0}$.
	- $X_{+}$é fechado para as funções de $F$ pois para todo $i$ tal que $X_{i}\in X_{+}$, sempre existirá um $X_{i+1}$ tal que $X_{i+1}= X_{i}\cup\{f(w_{1},\cdots,w_{k}) \mid w_{1},\cdots, w_{k} \in X_{i}\}$. Portanto $f$ aplicado à $X_{i}$ sempre pertence a $X_{+}$.
- $(ii)$ $X_{+} \subseteq X^{+}$
	- Vamos fazer uma prova por indução, como $X_{+}$ é definido como a união de conjuntos $X_{i}$ onde $i \ge 0$, queremos mostrar que $\forall i, X_{i} \subseteq X^{+}$.
	- Caso base: ($i=0$):
		- Como $X_{+}$é indutivo e $X_{0} = X$, $X_{0}\subseteq X^{+}$
	- Passo indutivo:
		- Hipótese Indutiva: $X_{n}\subseteq X^{+}$
		- Tese: $X_{n+1}\subseteq X^{+}$
			- Pela definição, $X_{n+1}= X_{n}\cup \{f(w_{1},\cdots,w_{k}) \mid w_{1},\cdots,w_{k} \in X_{n}\}$, $X_{n+1}$ é a união de $X_n$ com as funções de $F$ aplicadas à $X_{n}$, pela H.I, como $X_{n} \subseteq X^{+}$ e como $X_{+}$ é indutivo sobre $X$ e $F$, $X_{+}$ é fechado para as funções de $F$, portanto a segunda parcela também está contida em $X^{+}$.
Portanto a prova está concluída.

