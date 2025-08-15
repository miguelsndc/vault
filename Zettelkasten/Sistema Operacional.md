---
tags: arqcomp
---

Um sistema operacional possui algumas definições, entre elas cabe destacar duas:
- Uma "top-down", onde vê-se o sistema operacional como uma camada de abstração para os programadores de aplicativos interagirem com o hardware mais facilmente.
- Uma "bottom-up", onde o sistema operacional é um gerenciador de recursos que vai orquestrar todos os componentes de hardware de um computador para que ele funcione corretamente

Existem vários tipos de sistemas operacionais, entre eles:
- de grande porte: os "**mainframes**", que executam em computadores enormes do tamanho de salas, que possuem milhões de gigabytes de memória, e são excepcionalmente bons em processar quantidades enormes de entradas e saídas, geralmente possuem 2 tipos de processamento: **Em lote**, onde o sistema processa coisas sem um usuário presente, e a unidade de trabalho é pequena, podendo ser executadas várias ao mesmo tempo, ou **em tempo compartilhado**, onde vários usuários remotos compartilhem o uso do sistema, como para fazer consultas em bancos de dados
- Sistemas operacionais **embarcados**: são sistemas que rodam em dispositivos que não costumam ser vistos como computadores, como um micro-ondas por exemplo, e tem a certeza de que novos softwares nunca serão instalados, então todo o sistema pode ser armazenado em **ROM** (Read-Only-Memory), simplificando o design.
- Sistemas de **tempo real**: que podem ser divididos entre críticos e não-críticos, além disso, executar uma tarefa (ou concluí-la) num determinado intervalo de tempo é de absoluta importância, os sistemas de tempo real às vezes são pequenas bibliotecas conectadas com os aplicativos, sem nenhum proteção entre si, existe uma certa **sobreposição** entre sistemas portáteis, embarcados e de tempo real, já que todas elas possuem algum aspecto de tempo real não crítico. 

### Conceitos

**[[Processo]]**: é um contêiner que encapsula tudo que é necessário para a execução de um programa, um processo possui um programa executável, um **[[Espaço de Endereçamento]]** que é uma lista de posições da memória de 0 até algum máximo, onde o processo pode ler e escrever, os seus dados e sua **pilha**, além do ponteiro de pilha, alarmes pendentes, entre outras coisas. Em dado momento o sistema operacional pode decidir pausar a execução de um processo para dar vez à outro, dado que ele ocupou tempo suficiente de CPU. Portanto, é necessário guardar as informações sobre este processo de tal forma que ao ser reiniciado, todas as informações são preservadas e o estado é reestabelecido, o sistema operacional utiliza uma **tabela de processos**, que é um arranjo de estruturas que guarda essas informações para cada processo.
Um processo pode criar um ou mais processos filhos, dando origem à uma estrutura de árvore, e esses processos relacionados precisam de alguma [[Comunicação de Processos (IPC)]], para transmitir informações entre si, um processo também pode fazer [[Chamadas de Sistema]] para se autofinalizar, para requisitar mais memória, etc.


**Proteção**: também faz parte do papel do sistema operacional proteger arquivos e recursos com permissões designadas para cada tipo de usuário, no **UNIX**, as permissões são gerenciadas por $9$ bits, 3 para cada o administrador, 3 para os usuários do grupo do proprietário, e mais 3 para um usuário qualquer, esses bits são chamados de **bits rwx**, por exemplo, *rwxr-x--x* indica que o admin pode **ler: r**, **escrever: w** e **executar: x** arquivos, usuários quaisquer podem apenas executar, mas não ler e escrever.

### Estruturas

**Monolítico**: Neste arquitetura, todo o sistema operacional é ligado a um único binário executável, todas as rotinas são visíveis para todas as rotinas do sistema, não há nenhuma separação, todas as rotinas podem chamar todas as outras, o que torna complexo e difícil de compreender. Porém é possível haver estrutura num sistema monolítico, colocando-se os parâmetros das [[Chamadas de Sistema]] num local bem definido, como uma pilha por exemplo, e executando uma instrução de desvio de controle, passa-se para o modo núcleo e se dá o controle para o sistema operacional, que os busca e determina qual instrução será executada, então indexa uma tabela que contém na k-ésima linha um ponteiro para a rotina que executa a k-ésima chamada de sistema, então, tem-se a seguinte estrutura:
- Um programa principal que invoca as rotinas de serviço.
- Um conjunto de rotinas de serviço que executam as chamadas de sistema
- Um conjunto de rotinas utilitárias que auxiliam as rotinas de serviço

**Camadas**: A Arquitetura em camadas separa as responsabilidades em níveis, onde quanto mais baixo o nível, mas privilegiadas/críticas são as rotinas realizadas pela camada, e menor o nível de abstração. Cada camada é construída a partir da anterior, adicionando novas rotinas e disponibilizando outras para as camadas acima. Um exemplo seria um sistema com 6 camadas, sendo:
- **Camada 0**: Alocação de processador e multiprogramação;
- **Camada 1**: Gerenciamento de memória e tambor;
- **Camada 2**: Comunicação operador-processo;
- **Camada 3**: Gerenciamento de entrada/saída;
- **Camada 4**: Programas de usuário;
- **Camada 5**: Operador.
Que é a arquitetura do sistema do mano Djisktra.

**Micronúcleos**: Na arquitetura de micronúcleos, tenta-se minimizar o número de processos executando em modo núcleo ao estritamente necessário, para aumentar a confiabilidade do sistema. Tendo em vista que um erro introduzido em um processo rodando no modo núcleo, pode facilmente referenciar um endereço inválido na memória e explodir o sistema operacional inteiro. As rotinas do núcleo são realizadas por um processo chamado de micronúcleo, que realiza operações básicas como chavear processos e oferece uma interface de chamadas de sistema. Um sistema em micronúcleos altamente modularizado tem a vantagem de que um processo dando pau, um driver de dispositivo por exemplo, de áudio, o som é truncado, e o sistema continua tendo seus outros processos funcionando.