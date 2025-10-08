---
tags: teorica
---

Expressões regulares são uma forma mais sucinta de expressar linguagens:

*Dizemos que $R$ é uma expressão regular, se $R$ for:*
1. a$ para algum $a$ no alfabeto $\Sigma$
2. $\epsilon$  
3. $\emptyset$
4. $(R_{1} \cup R_{2})$ onde $R_1$ e $R_2$ são expressões regulares
5. $(R_{1} \circ R_{2})$ onde $R_{1}$ e $R_{2}$ são expressões regulares, o
6. $(R_{1}^{*})$ onde $R_{1}$é uma expressão regular

$\epsilon$ e $a$ representam as linguages $\{\epsilon\}$ e $\{a\}$, e o item $3$ representa a linguagem vazia, preste atenção pois $\epsilon$ é a linguagem que contém a cadeia vazia, e $\emptyset$ é a linguagem vazia.

> [!danger]
> Ruy avisou que definir expressões regulares com o $\Sigma$ não faz sentido, então não use, faça a união das linguagens unitárias ou use o conjunto.


##### Identidade

Seja $R$ uma expressão regular, então:

- $R \circ \epsilon = R$
- $R \cup \emptyset = R$

Perceba que concatenar a cadeia vazia com outra cadeia não muda a cadeia anterior, e unir uma linguagem à linguagem vazia é o mesmo que unir com o conjunto vazio, não muda nada, porém:

- $R \cup \epsilon \ne R$ , porque se $R = 0$ por exemplo, então $L(R) = \{0\}$ e $L(R \cup \epsilon) = \{0, \epsilon\}$.
- $R \circ \emptyset \ne R$ , porque se $R = 0$ por exemplo, então $L(R) = \{0\}$ e $L(R \circ \emptyset) = \emptyset$.

Perceba que a operação de concatenação necessita que haja pelo menos uma cadeia em ambas linguagens, se não, não há com o que concatenar, e obtemos a linguagem vazia como descrito acima.