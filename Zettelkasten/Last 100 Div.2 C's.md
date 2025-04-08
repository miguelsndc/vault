---
tags: div2c's
---

1014C - **Asuna and Mosquitoes**

pensei inicialmente em só jogar todos os impares dentro dos pares e pegar o maior, mas nao funciona pq eu posso sempre pegar um zero e tirar 1 de 1 impar e depois juntar esse par q sobrou com um impar maior. Acontece que esse processo é exatamente somar todos os numeros, tirar a quantidade de impares e depois diminuir, pq pra cada impar q eu for juntando com um par, no final das contas vai sobrar alguns pares e varios 1's, que sao a quantidade de impares pq é ótimo eu tirar 1 com algum 0 e depois somar em outro impar.

1012C - Dining Hall

Não consegui pensar em nada, olhei o editorial, não entendi, olhei os códigos submitados e ainda não entendi (?).

Aparentemente a ideia da solução q foi submitada é manter:
- 3 variaveis indicando a celula (x, y) e a distancia pra celula da mesa vazia mais próxima
- uma heap indicando quais as celulas vazias mais próximas 
Pra conseguir lidar com os dois tipos de queries

Quando vem uma query to tipo 1 (celula mais proxima)
- se tiver algo na priority queue e se esse algo tiver uma distancia menor q a distancia pra tabela vazia mais próxima ele joga esse cara lá
- ele coloca o cara na tabela vazia e joga na priority queue as tres celulas da tabela dessa celula junto com suas respectivas distancias, então ele faz uma formula pra pegar a próxima tabela mais próxima **vazia**: que é
- 
```cpp
ans[i] = {x, y};
pq.push({x + y + 1, x + 1, y});
pq.push({x + y + 1, x, y + 1});
pq.push({x + y + 4, x + 1, y + 1});
if (y == 1) swap(x, y), y += 3;
else x += 3, y -= 3;
dis = x + y;
```

joga na heap as celulas e as distancias, então ele pega a celula e joga na proxima tabela mais próxima, a celula q ele pega sempre é a da ponta inferior esquerda, pq é a mais proxima da origem sempre, com esse zigzag ele sempre pega a tabela mais próxima.

2085C - Serval and The Formula

Notando que a formula pode ser reescrita como (x + k) & (y + k) = 0, podemos fazer o seguinte, pegamos o maior numero e achamos a primeira potencia de 2 maior ou igual ao numero e a resposta é essa potencia de 2 menos o numero, porque como o maior continua sendo o maior independente de quantos somamos a ele, como uma potencia de 2 só tem 1 bit, o outro número vai ter o msb = 0, então o and vai dar 0, caso os numeros sejam iguais sempre vai ter 1 bit igual, entao nao vai dar pra encontrar.

> Primeira questão que resolvo só com o hint, tendo derivado já a primeira hint.

