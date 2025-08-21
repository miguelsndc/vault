---
tags: arqcomp
---

$1)$ A frase indica que muitos programas não foram escritos para utilizar os recursos de multiprocessadores, e possuem uma premissa de uniprocessamento, já que é mais fácil e barato de implementar.

$2)$ 
$a)$ **Particionamento/Balanceamento** -  A carga de trabalho deve ser devidamente particionada/balanceada entre os múltiplos processadores, para evitar que um subconjunto limitado deles esteja trabalhando demais e outros de menos, desperdiçando a CPU de vários processadores enquanto superutiliza alguns.

$b$) **Coordenação/Sincronização** - Por muitas vezes deseja-se que processadores trabalhem em partes diferentes do problema, então eles devem estar devidamente coordenados e sincronizados, para evitar que trabalho seja refeito ou perdido, ou nunca sequer feito.

$c)$ **Comunicação** Por diversas vezes deseja-se que os processadores dividam o trabalho e se comuniquem por algum espaço de memória compartilhado, isso introduz uma série de problemas como: informações perdidas, atualizações perdidas, condições de corrida, processadores realizando trabalho com informações desatualizadas, inconsistência de dados, e assim por diante.

$3)$ 
A **Taxonomia de Flynn** categoriza os processadores paralelos em quatro categorias, sendo elas:
- **SIMD** - **S**ingle **I**nstruction, **M**ultiple **D**ata: uma única instrução de máquina controla a execução simultânea de uma série de elementos de processamento em operações básicas.
- **MIMD** - **M**ultiple **I**nstruction **M**ultiple **D**ata: Um conjunto de processadores executa diferentes instruções em múltiplos conjuntos de dados ao mesmo tempo.
- **SISD** **S**ingle **I**nstruction **S**ingle **D**ata: Um processador único executa uma única instrução por vez em um conjunto de dados.
- **MISD** - **M**ultiple **I**nstruction **S**ingle **D**ata: Uma sequência de dados é transmitida para um conjunto de processadores onde cada um executa uma sequência de instruções.

$4)$ Principais caraterísticas de sistemas **SMP** (Symmetric Multiprocessores) são:
- $\ge 2$ processadores de capacidade igual ou semelhante
- Compartilham a memória principal e recursos de IO
- Tempo de acesso â memória é igual para todos os processadores **UMA** *Uniform Memory Access*.
- Processadores desempenham a mesma função
- S.O oferece interação entre processadores à nível de arquivos, dados compartilhados e tarefas.

$5)$ A carga de trabalho é evidentemente dividida igualmente entre os processadores, dado que são semelhantes e executam a mesma tarefa.
A disponibilidade é maior, dado que temos vários processadores executando a mesma tarefa, e se um falhar, a carga de trabalho é redirecionada para os outros. 
Escala melhor, já que basta adicionar mais processadores para aguentar mais trabalho.

$6)$ O barramento compartilhado é um middle-man entre a memória e os processadores, porém um grande limitador de performance, já que todo acesso à memória de todos os processadores passa por ele, uma melhoria é a inclusão de uma cache para cada CPU, onde ela primeiro busca na cache, em caso de miss aí sim o barramento é necessário. Mas isso introduz problemas de coerência de cache entre os processadores e consistência com a memória. Então entram políticas de escrita de cache.

$7)$ 

$8)$ Clusters são redes de múltiplos computadores interligados (nós) que se comunicam através de uma rede de interconexão, WAN ou LAN.

$9)$ Vantagens de clusters são:
- **Escalabilidade absoluta**: um cluster pode ter dezenas, centenas ou até milhares de máquinas trabalhando juntas.
- **Escalabilidade incremental**: é possível incrementar o cluster aos poucos, adicionando novas máquinas conforme for necessário.
- **Alta disponibilidade**: falha em um nó não implica na falha do sistema, todos os outros continuam rodando.
- **Preço/desempenho**: É possível montar um cluster com desempenho igual ou superior a uma máquina de grande porte, com custo menor.

$10)$ 
**Clusters com servidores passivos** tem a característica de que uma máquina principal executa todo o trabalho, caso ela falhe, uma máquina secundária assume e assim por diante. É fácil de implementar porém é extremamente ineficiente e desperdiça o poder de processamento de todas as outras $n -1$ máquinas disponíveis no cluster.

**Clusters com servidores ativos** mantém todas as máquinas trabalhando em conjunto, o que é muito melhor em questão de desempenho, porém a **complexidade** de se implementar e manter um sistema nesse modelo é muito superior.
