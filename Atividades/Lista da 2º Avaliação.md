---
tags: md
---
> [!faq] 1 Questão
> Os monitores de MD estavam jogando UNO, e decidiram criar uma regra de trincas para dinamizar o jogo. A regra de trincas consiste em poder jogar três cartas de uma vez, mas essas precisam ser apenas uma sequência numérica da mesma cor (Ex.: 1, 2 e 3 vermelhos), ou cartas de mesmo número e cores diferentes. Considerando que há apenas cartas numéricas (que vai de 0 a 9), e 4 cores  diferentes (vermelho, azul, amarelo e verde), de quantas formas  é possível formar uma trinca?
>

Dividindo a sequência de $0$ a $9$ em grupos de três números consecutivos, teremos $8$ grupos: $012,123,234,345,456,567,678,789$, portanto temos $8 \choose 1$ formas de escolher uma trinca de uma cor, para as $4$ cores, há ${8\choose 1} \cdot 4= 8\cdot 4 = 32$ formas. Para cartas de mesmo número e cores diferentes, há $4\choose3$ formas de escolher um trio de números iguais de três dos quatro conjuntos. Para os $10$ dígitos: ${4 \choose 3} \cdot 10=4\cdot10=40$. No total há $32+40=72$ formas de formar uma trinca.
___

Gendelf, o Ciano,  ́e um mago muito respeitado que est ́a agora na sua cidade! Ele tem um truque de adivinhação que consiste em escolher ao acaso 4 números (sem reposição) dentre um total de 6 números positivos e 8 negativos. A tarefa do nosso camarada nórdico é predizer se o número resultante da multiplicação desses 4 números é positivo ou negativo. Ajude nosso amigo feiticeiro e responda em quantos casos poss ́ıveis o n ́umero resultante é positivo?