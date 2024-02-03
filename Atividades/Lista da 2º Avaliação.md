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

Existem $n$ alunos e $n$ monitores. Suponha que queremos escolher $m$ elementos de ambos, com $0 \le m \le n$. Suponha que escolhemos $k$ alunos, com $0 \le k\le m$, logo precisamos escolher mais $m-k$ monitores. então, temos ${m \choose k}{m \choose m-k}$ formas de fazer isso. Pela identidade:
$$\begin{align*}
\sum\limits_{k=0}^{m}{m\choose k}{m\choose m-k}&= \sum\limits_{k=0}^{m}{m\choose k}^{2}={m+m\choose m}= {2m \choose m}
\end{align*}$$
Para qualquer $0 \le m \le n$. Caso $m=n$ então há $2n \choose n$ formas.
___
> [!faq] 4 Questão
> Encontre o coeficiente de $x^{14}y^{10}$ na expansão de $(3x\sqrt{x^{2}-1} + 2y)^{20}$.

Os coeficientes são dados por $$\begin{align*}
\sum\limits_{j=0}^{20}{20 \choose j}(3x\sqrt{x^{2}-1})^{20-j}(2y)^{j}
\end{align*}$$
Para $x^{14}y^{10}$ temos que ter $j=10$, logo:
$$\begin{align*}
{20 \choose 10}(3x\sqrt{x^{2}-1})^{10}(2y)^{10}&= {20\choose10}(3x)^{10}(x^{2}-1)^{5}2^{10}y^{10}\\
&= {20\choose10}3^{10}2^{10}x^{10}y^{10}(x^{2}-1)^{5}
\end{align*}$$
Expandindo $(x^{2}-1)^{5} = x^{10}-5x^{8}+10x^{6}-10x^{4}+5x^{2}-x^{2}$:
$$\begin{align*}
&{20 \choose 10}3^{10}2^{10}x^{10}y^{10}(x^{10}-5x^{8}+10x^{6}-10x^{4}+5x^{2}-x^{2})\\
\end{align*}$$
O único coeficiente que nos dá $x^{14}$ e $y^{10}$ ao mesmo tempo é $-10x^{4}$, descartando os outros, temos que o coeficiente de $x^{14}y^{10}$ é:
$$\begin{align*}
&-{20 \choose 10}10\cdot6^{10}x^{14}y^{10}\\
&\therefore-{20 \choose 10}10\cdot6^{10}
\end{align*}$$
  ___
> [!faq] Questão
> Encontre quantos números no intervalo $[1, 1387]$ são relativamentos primos à $30$:
> 

Como $30 = 2\cdot3\cdot5$, todo número $k$ onde $k\in [1,1387]$ **não** pode ter fatores $2$ ou $3$ $ou$ 5.
Há $\lfloor\frac{1387}{2} \rfloor = 693$ números pares, desses, $\lfloor \frac{693}{3} \rfloor = 231$ são divisíveis por $3$. 
Há $\lfloor \frac{1387}{3} \rfloor = 462$ números divisíveis por $3$, desses $\lfloor \frac{462}{5} \rfloor = 92$ são divisíveis por $5$
Há $\lfloor \frac{1387}{5} \rfloor = 277$ números divisíveis por $5$, desses, $\lfloor \frac{277}{2}\rfloor =138$ são pares.
Há $\lfloor \frac{1387}{30} \rfloor =46$ números divisíveis por $30$.

Logo, há $1387 - 693 - 462 - 277  + 231 + 92 + 138 + 46 = 370$ números relativamente primos à $30$ no intervalo $[1, 1387]$.
___
> [!faq] Questão
> Um algoritmo de compressão de dados é dito sem perdas se os dados originais podem ser unicamente reestruturados a partir dos dados comprimidos, ou seja, se existe função inversa bem definida. Vendo algoritmos de compressão de dados como funções $f:\Sigma \rightarrow \Sigma$ onde $\Sigma$  é o conjunto das strings binárias (sequências de 0’s e 1’s) de tamanho finito, prove que não existe algoritmo de compressão de dados sem perdas onde $|f(x)| ≤ |x|$ para todo $x \in \Sigma$, com $|x|$ denotando o comprimento da string $x$. P.S.: No contexto do problema, para todo algoritmo $f$, existirá pelo menos um $x$ tal que $|f(x)| < |x|$, já que é um algoritmo de compressão.

Existem $2^{|\Sigma|}$ possíveis bit strings, suponha que exista uma string $x \in \Sigma$ que após a compressão tenha tamanho $y$ tal que $y \lt |x|$ e que todas as outras $x' \in \Sigma$ tenham seu tamanho $|x'|$ menor ou igual ao de antes da compressão. logo existem no máximo $2^{|\Sigma|-1}$ strings no contradomínio. Pelo princípio da casa dos pombos existem pelo menos duas strings diferentes que vão ter a mesma string como resultado da compressão, ou seja: existe $a,b\in \Sigma \mid a\ne b$  $f(a)=f(b)$,  logo não pode haver função inversa e o algoritmo é impossível.
___
> [!faq] Questão
> Encontre um inteiro $i$ tal que $i^{2} - 3i - 19$ é divisível por $289$ ou prove que este inteiro não existe.

Para $i$ ser divisível por $289$, a congruência $i^{2}-3i-19\equiv 0 \pmod{289}$ deve ser satisfeita para algum inteiro $i$.
$$\begin{align*}
i^{2}-3i \equiv 19\pmod{289}
\end{align*}$$




