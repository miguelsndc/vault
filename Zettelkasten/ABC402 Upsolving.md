---
tags: maratona
---

> A and B went smoothlyj

### C - Dislike Foods -  [link](https://atcoder.jp/contests/abc402/tasks/abc402_c)

Takahashi era frango e nao gostava de um monte de ingredientes,cada comida tem um conjunto distinto de ingredientes, a cada dia que passa takahashi desaviada com um ingrediente, tu tem que printar, pra cada dia, quantas comidas ele pode comer se ele desaviadar com o ingrediente $b[i]$.

Tentei pensar num brute force mas não tem como com as constraints, (tudo $\le 3 \cdot10^{5}$), seria pra cada dia passar por cada comida e deletar o ingrediente, o que é $O(N M \Sigma k_{i} )$, que basicamente cubico.

A questão é que uma comida só se torna disponivel quando o ultimo ingrediente que ela tem, na ordem dos $b[i]$ é consumido, então pra cada comida eu só tenho que saber qual a ultima posição em b que é um ingrediente dessa comida, então é só somar quando chego lá, pode se usar um vetor e ir fazendo uma soma acumulada.

### D - Line Crossing - [link](https://atcoder.jp/contests/abc402/tasks/abc402_d)

Basicamente dado um circulo com n pontos distribuidos igualmente ao redor do circulo e m pares de pontos, uma reta é traçada entre cada par, vc tem que descobrir quantos pares de retas se intersectam.

Percebi com ajuda do google que podia fazer $no\_total\_pares\_retas- no\_pares\_paralelas$, então vc só precisa calcular quantas retas são paralelas. tentei rotacionar o $(0,1)$ pra achar os pontos, deu certo, tentei achar as retas e deu certo também, mas na hora de achar as retas parelelas acabei tropeçando em erros de precisão, tentei usar fmod mas não deu certo, sempre faltava 1 ou 2, entãoo contest acabou, a ideia estava totalmente certa, mas a solução foi falha, acontece que um par de números é paralelo se a soma deles mod n por igual ?
- Funciona por que as retas definidas por pontos $a_{i}$ e $b_{i}$ se contarmos o k-esimo ponto no sentido horario de $a$ e  o kesimo ponto no sentido antihorario por $b$, essas retas são paralelas, por exemplo com n = 6, as retas (1,5) e (2,4) são paralelas. devia ter pensado nisso, talvez encarando o suficiente eu teria descoberto o mod n.

--- 
> A partir daqui não li no contest

### Payment Required

Takahashi tem um contest com n problemas, com orçamento $x \le 5000$ $n \le 8$, cada um tem um valor $S[i]$, custo $C[i] \le 5000$ e probabilidade de acerto $P[i]$,  maximize o valor esperado the pontos dado que takahashi escolhe as submissões que maximizam esse valor.

Não acertei nem fudendo e nem conseguiria fazer em contest, tentei um knapsack, mas era bitmask, parecia muito um knapsack mas recuperar a questão do valor esperado com o knapsack é bem tricky, a solução é com bitmask:

Considere uma DP: pra algum $T \subset \{1, 2, \cdots, N\}$ e $0 \le x \le n$, seja $dp[T][x]$ o maior valor esperado caso ele tenha resolvido os problemas em $T$ e tem $x$ yen sobrando.

As recorrências:

Se ele submita um problema $i, i \notin T, x \ge C[i]$ ele resolve com probabilidade $P[i]$ e **não resolve** com probabilidade $(1 - P[i])$. então é o maior valor esperado possível é:
$$\begin{align*}
P_{i} \cdot(S_{i} + dp[T \cup \{i\}][x - C_{i}]) + (1-P_{i})(dp[T][x - C_{i}])
\end{align*}$$
Isto é, o valor esperado é a soma de:
- Ele resolvendo o problema i que ele não resolveu, então a união do conjunto atual e o custo descontado da capacidade atual, tudo vezes a probabilidade disso acontecer, **ou**:
- ele não resolve e vc só desconta o custo
Somando por que os eventos são independentes, e a probabilidade de um **ou outro** acontecer é a soma das probabilidades desses eventos.

**A recorrência é definida por $dp[T][x]$, se começarmos o jogo resolvendo T problemas com x yen sobrando, e jogarmos otimamente, qual o maior valor esperado ?, dada essa definição, a resposta está em $dp[0][X]$, porque não resolvemos nada e temos todo o dinheiro, se definirmos por, yens gastos, a resposta estaria em $dp[0][0]$ (AC)**

Com DP talvez seja util, dado o que você quer, pensar no inverso e tentar chegar do inverso a partir do estado atual.
	
> Desenhar a recorrência pra problemas de dp bitmask pode ser util pra visualizar as recorrências
