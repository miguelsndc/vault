---
tags: md
---
> [!faq] 1 Questão
> Os monitores de MD estavam jogando UNO, e decidiram criar uma regra de trincas para dinamizar o jogo. A regra de trincas consiste em poder jogar três cartas de uma vez, mas essas precisam ser apenas uma sequência numérica da mesma cor (Ex.: 1, 2 e 3 vermelhos), ou cartas de mesmo número e cores diferentes. Considerando que há apenas cartas numéricas (que vai de 0 a 9), e 4 cores  diferentes (vermelho, azul, amarelo e verde), de quantas formas  é possível formar uma trinca?
>

Dividindo a sequência de $0$ a $9$ em grupos de três números consecutivos, teremos $8$ grupos: $012,123,234,345,456,567,678,789$, portanto temos $8 \choose 1$ formas de escolher uma trinca de uma cor, para as $4$ cores, há ${8\choose 1} \cdot 4= 8\cdot 4 = 32$ formas. Para cartas de mesmo número e cores diferentes, há $4\choose3$ formas de escolher um trio de números iguais de três dos quatro conjuntos. Para os $10$ dígitos: ${4 \choose 3} \cdot 10=4\cdot10=40$. No total há $32+40=72$ formas de formar uma trinca.
___

> [!faq] 2 Questão
> Gendelf, o Ciano, é um mago muito respeitado que está agora na sua cidade! Ele tem um truque de adivinhação que consiste em escolher ao acaso 4 números (sem reposição) dentre um total de 6 números positivos e 8 negativos. A tarefa do nosso camarada nórdico é predizer se o número resultante da multiplicação desses 4 números é positivo ou negativo. Ajude nosso amigo feiticeiro e responda em quantos casos poss ́ıveis o n ́umero resultante é positivo?

Para alcançar seu objetivo, o grande Gendelf, o Ciano, deve escolher um número par de números negativos, então, considerando os casos:
1. $0$ números negativos: ${6\choose4} = 15$
2. $2$ números negativos: ${6\choose 2}\cdot{8\choose2} = 420$
3. $4$ números negativos: ${8 \choose 4}= 70$
Logo Gendelf tem um número negativo em $15+420+70=505$ casos.
___
> [!faq] 3 Questão
> Dados $n$ alunos e $n$ monitores, prove que existem $2n \choose n$ possibilidades ao selecionar uma quantidade arbitrária ($0$ até $n$) deles, sabendo que ao selecionar um número $k$ de alunos é necessário selecionar $k$ monitores. $\rm{OBS}$ utilize a identidade:
> $$\sum_{k=0}^{n}{r \choose k}{s \choose n-k}= {r+s \choose n}$$

Existem $n$ alunos e $n$ monitores. Suponha que queremos escolher $m$ elementos de ambos, com $0 \le m \le n$. Suponha que escolhemos $k$ alunos, com $0 \le k\le m$, logo precisamos escolher mais $m-k$ monitores. então, temos ${m \choose k}{m \choose m-k}$ formas de fazer isso. Pela identidade de [[Vandermonde's Identity|vandermonde]]: 
$$\begin{align*}
\sum\limits_{k=0}^{m}{m\choose k}{m\choose m-k}&= \sum\limits_{k=0}^{m}{m\choose k}^{2}={m+m\choose m}= {2m \choose m}
\end{align*}$$
Para qualquer $0 \le m \le n$. Caso $m=n$ então há $2n \choose n$ formas.