---
tags: arqcomp
---

$1)$ A frase indica que muitos programas não foram escritos para utilizar os recursos de multiprocessadores, e possuem uma premissa de uniprocessamento, já que é mais fácil e barato de implementar.

$2)$ 
$a)$ **Particionamento/Balanceamento** -  A carga de trabalho deve ser devidamente particionada/balanceada entre os múltiplos processadores, para evitar que um subconjunto limitado deles esteja trabalhando demais e outros de menos, desperdiçando a CPU de vários processadores enquanto superutiliza alguns.

$b$) **Coordenação/Sincronização** - Por muitas vezes deseja-se que processadores trabalhem em partes diferentes do problema, então eles devem estar devidamente coordenados e sincronizados, para evitar que trabalho seja refeito ou perdido, ou nunca sequer feito.

$c)$ **Comunicação** Por diversas vezes deseja-se que os processadores dividam o trabalho e se comuniquem por algum espaço de memória compartilhado, isso introduz uma série de problemas como: informações perdidas, atualizações perdidas, condições de corrida, processadores realizando trabalho com informações desatualizadas, inconsistência de dados, e assim por diante.

$3)$ 

- **SIMD** - **S**ingle **I**nstruction **M**ultiple **D**ata