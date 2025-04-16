---
tags: maratona
---

# Feitas

C - Bacteria

Deve haver um upper bound pra quantidade de operações que devem ser feitas, chutei 10⁶ durante o contest mas eu acho que duas ou tres operações e continuar com 2 elementos na priority queue ja deve quebrar, submitando aparentemente o limite é 4 operaçoes.

F - Tickets

É literalmente so fazer, sorta o input e itera de 1 ate 10⁶ calculando o valor pra cada cara, mantem um vetor de pontos pra saber quantos cada score possivel tem $[0, 27]$, depois é só responder as queries em ordem, tranquilo.

I - Heist

O cabra nao lembra nem do x e nem do numero de teclados presentes, a gnt tem que assumir o x como sendo o menor numero, caso contrario tem um numero presente q não faz parte dos teclados do input, o q é uma contradição, entao os teclados roubados simplesmente sao a diferença dos adjacentes quan

J - Buying a TV Set

Resolvi esse totalmente na sorte, mas pra calcular o numero de pares w e h tais que w <= a e h <= b e w/h = a/b a gnt primeiro divide pelo gcd pra deixar irredutivel, depois é so pegar o minimo de w/a e h/b, que vai ser a quantidade de numeros q tem essa razao.


> Um dos meus grandes probelmas é ver que varias pessoas tao resolvendo uma certa questao, e ver que eu nao sei imediatamente como resolver, entao eu entro em panico e começo a tentar qualuqer coisa, tomar wa, coisas que eu **sei** que não vao passar, só pra nao "ficar pra trás", ou melhor, sentir que não estou ficando pra trás, preciso mudar isso, por enquanto, nao olhe os standing sob nenhuma hipótese, olhe somente as contagens de resolução caso, e **somente caso** esteja estagnado. 


K - Median Partitions

era **DP**, entao esquece resolver sozinho, uma soluçao q achei foi $dp[i]$ = numero maximo de subarrays bons que terminam em i, pra um subarray de tamanho *len* ser bom ele precisa ter no maximo $(len + 1)//2$ elementos menores q $m$, pq a mediana é pega sortando.

entao pra cada $i$ de $1$ ate $n$, a gente passa por todos os subarrays, usa uma prefix sum pra saber se o subarray é bom rapido. Então caso seja bom:
- se j == 0, é pq o subarray desde o começo até i é bom, entao dp daquela posiçao vai ser o maximo q tem la e $1$.
- caso j > 0, entao o subarray j..i é bom, a gente so pode considerar esse subaray se tiver alguma partição de 1 ate j q seja boa também, porque se nao a gente quebra a condição da dp, entao se dp de j for maior q zero, a gente bota em i o maximo entre dp de i e dp de j + 1, + 1 sendo o subarray q foi adicionado nessa iteração.
Bem compreensível, preciso praticar dp. isso é do caralho pra falar a verdade, não sei porque eu evito tanto dp, se eu inventasse isso do zero e tomasse AC de primeira eu acho que eu me gozava nas calças

A - Coffe Break

Bem resolvível, pensei 10 minutos e codei, tomei 2 was por usar a função lowerbound do std ao inves da interna do set, mas a ideia é basicamente manter um set de pairs onde o segundo indice é o indice do valor no array, manter duas variaveis pra saber o dia atual e o valor atual de minutos q vc quer, e enquanto que o set nao tiver vazio vc faz:
- pega o lowerbound do valor atual e se for menor q m vc bota na resposta, apaga esse valor e busca outro lower bound pra valor + d + 1, que é quando ele vai conseguir tomar outro café
- depois q isso passar ou q nao houver mais ninguem <= m, vc bota o valor pra 0 dnv pra começar outro dia, e aumenta o dia atual
nlogn facil.

