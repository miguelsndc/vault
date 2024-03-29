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
Há $\lfloor\frac{1387}{2} \rfloor = 693$ números pares, desses, $\lfloor \frac{693}{3} \rfloor = 231$ são divisíveis por $3$,
$\lfloor \frac{1387}{3} \rfloor = 462$ números divisíveis por $3$, desses $\lfloor \frac{462}{5} \rfloor = 92$ são divisíveis por $5$,
$\lfloor \frac{1387}{5} \rfloor = 277$ números divisíveis por $5$, desses, $\lfloor \frac{277}{2}\rfloor =138$ são pares,
e $\lfloor \frac{1387}{30} \rfloor =46$ números divisíveis por $30$.

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
i^{2}-3i -19&\equiv0\pmod{17}\\
\end{align*}$$
Como $289 = 17^{2}$ eu posso checar divisibilidade por $17$:
$$\begin{align*}
i^{2}-3i - 19 &\equiv 0 \pmod{17}\\
i^{2}-3i &\equiv 19 \pmod{17} \text{ Multiplicar por 4}a\\
4i^{2}-12i &\equiv 76 \pmod{17} \text{ Completar os Quadrados}\\
4i^{2}-12i + 9 &\equiv 85 \pmod{17} \text{ Fatorar }\\
(2i-3)^{2} &\equiv 85 \pmod{17}\\
(2i-3)^{2} &\equiv0 \pmod{17} \text { Tecnicamente eu posso elevar a }\frac{1}{2}\\
2i &\equiv 3 \pmod{17}\\
18i &\equiv 27 \pmod{17}\\
i &\equiv10 \pmod{17}
\end{align*}$$
Logo $i = 17k + 10$ então:
$$\begin{align*}
(17k+10)^{2}-3(17k +10)-19 &\equiv 0 \pmod{289}\\
10^{2}-3(10)-19 &\equiv 0 \pmod{289}\\
51 &\equiv 0 \pmod{289}
\end{align*}$$
O que é uma contradição, logo não há inteiro que satisfaça as condições necessárias.
___
>[!faq] Questão
 	Um jogador de futebol chamado Claudino, tem uma meta exata de $759$ gols a ser cumprida na sua carreira. Porém um homem do futuro viu que Claudino terá $0$ gols na carreira. Contudo, ele pode mudar isso, já que sempre que ele assiste um vídeo completo do Cristiano Ronaldo ele muda o futuro e acrescente $28$ gols à sua carreira, e sempre que ele assiste um vídeo completo do Neymar ele muda o futuro e acrescenta $23$ gols à sua carreira. Liste todas as maneiras possíveis (quantos vídeos de cada jogador ele tem que assistir) para Claudino cumprir a meta exata de $759$ gols na carreira.

Claudino não sabe mas ele quer uma solução positiva para a equação diofantina:
$$\begin{align*}
28c + 23n &= 759
\end{align*}$$
Onde $c =$ número de vídeos do CR7 e $n=$ número de vídeos de Neymar.
Logo, temos:
$$\begin{align*}
28c+23n &= \gcd(28, 23)\\
(28,23) &\implies\\
28 &= 23\cdot1 + 5\\
23 &= 5\cdot4+3\\
5 &= 3\cdot1 + 2\\
3&= 2 \cdot 1 + 1\\
2 &= 2 \cdot 1
\end{align*}$$
Encontrando os coeficientes de Bezoút:
$$\begin{align*}
1&= 3- 2\cdot1\\
&= 3- (5-3)\\
&= 3(2)-5\\
&= (23-5\cdot4)(2) - 5\\
&= 23(2)-5(9)\\
&= 23(2)- (28 - 23)(9)\\
&= 23(11)-28(9) \\
&= 23(11)+28(-9)
\end{align*}$$
Logo os coeficientes são $11$ e $-9$, então temos:
$$\begin{align*}
23(11) + 28(-9) &= 1\\
23(8349) + 28(-6831)&= 759
\end{align*}$$
Porém assistir $-6831$ vídeos do neymar soa meio estranho, vamos ajudar Claudino encontrando uma solução positiva utilizando a forma paramétrica, então:
$$\begin{align*}
c &= -6831 + 23t\\
n&= 8349 -28t\\
\end{align*}$$
Apesar de podermos testar valores utilizando a forma paramétrica, é fácil perceber que $\frac{759}{23}=33$, logo Claudino pode assistir $33$ vídeos do neymar para alcançar sua meta, e todas as possíveis soluções são da forma:
$$\begin{align*}
28(-6831 + 23t) +23(8349-28t) &= 759 \;\;\forall t\in\mathbb{Z}
\end{align*}$$
___
>[!faq] Questão
>Se Iasmin retira bolas de futebol de um saco de $2, 3,4,5$ e $6$ por vez, restam, respectivamente, $1,2,3,4$ e $5$ bolas. Mas se as bolas são retiradas de $7$ em $7$,
 não resta nenhuma bola. Qual é o menor número de bolas de futebol que poderia ter no saco ?

Podemos expressar o problema como um sistema de congruências lineares, onde $x$ é a quantidade de bolas no saco:
$$\begin{align*}
&(I) \;\; &x \equiv 1 \pmod{2}\\
&(II) \;\; &x \equiv 2 \pmod{3}\\
&(III)\;\; &x \equiv 3 \pmod{4}\\
&(IV) \;\; &x \equiv 4 \pmod{5}\\
&(V) \;\; &x \equiv 5 \pmod{6}\\
&(VI)\;\; &x\equiv 0 \pmod{7}\\
\end{align*}$$
Comecemos com $VI:$ $x= 7k$, substituindo em $V$ temos $7k \equiv 5 \pmod{6} \implies k \equiv 5 \pmod{6} \therefore k=6k_{1} + 5$,
logo: $x = 7(6k_{1} + 5) = 42k_{1}+5$.
sub. em $IV$:
$42_{1}+35 \equiv 4 \pmod{5} \implies 2k_{1} \equiv -31 \pmod 5 \implies k_{1} \equiv 2 \pmod{5} \therefore k_{1}= 5k_{2}+2$
logo $x=42(5k_{2}+2)+35=210k_{2}+119$. 
sub em $III$:
$210k_{2}+119 \equiv 3 \pmod{4} \implies 210k_{2}\equiv-116 \pmod{4} \implies 2k_{2}\equiv 4 \pmod{4}$.
$\rm{MDC}(4,2)=2$, dividindo tudo por $2$ temos:
$k_{2}  \equiv 2 \pmod{2} \therefore k_{2} = 2k_{3}$.
logo $x=420k_{3} + 119$.
sub em $II$:
$420k_{3} + 119 \equiv 2\pmod{3} \implies 420k_{3}\equiv -117 \pmod{3} \implies k_{3}\equiv 0 \pmod{3}$
$\therefore k_{3}= 3k_{4}$
logo, $x = 1260k_{4}+119$.
sub em $I$:
$1260k_{4} + 119 \equiv 1 \pmod{2} \implies k_{4}\equiv 0 \pmod{2}$.
logo $x = 2520k_{4}+119$, portanto $x$ é da forma: $x \equiv 119 \pmod{2520}$, sendo o menor número que satisfaz essa congruência o próprio $119$.
___ 
>[!faq] Questão
>Mostre que $42$ divide $n^{7} - n$ sendo $n$ um número inteiro positivo.

Note que $42 = 2 \cdot 3 \cdot 7$, pelo Pequeno teorema de Fermat, $n^{7}\equiv n \pmod{7}$, logo $7 \mid n^{7}- n$ e $n^{7}-n$ é par, já que ambos $n$ e $n^{7}$ possuem a mesma paridade. Para demonstrar que é divisível por $3$, podemos notar que, pelo mesmo princípio:
$$\begin{align*}
n^{3} &\equiv n \pmod{3}\\
n^{6} &\equiv n^{2} \pmod{3}\\
n^{7} &\equiv n^{3}\pmod{3}\\
n^{7} &\equiv n^{3} \equiv n\pmod{3}\\
n^{7} &\equiv n\pmod{3}\\\\
&\therefore 3 \mid n^{7}- n
\end{align*}$$
Pelo Teorema fundamental da Aritmética, $n^{7} - n = 2\cdot 3 \cdot 7 \cdots$, e como $42 = 2 \cdot 3 \cdot 7$, $42$ divide $n^{7}- n$ para todo $n$ positivo.
___
