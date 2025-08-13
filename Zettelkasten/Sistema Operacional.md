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

[[Processo]]: é um contêiner que encapsula tudo que é necessário para a execução de um programa, um processo possui um programa executável, um **espaço de endereçamento** que é uma lista de posições da memória de 0 até algum máximo, onde o processo pode ler e escrever, os seus dados e sua **pilha**, além do ponteiro de pilha, alarmes pendentes, entre outras coisas. Em dado momento o sistema operacional pode decidir pausar a execução de um processo para dar vez à outro, dado que ele ocupou tempo suficiente de CPU. Portanto, é necessário guardar as informações sobre este processo de tal forma que ao ser reiniciado, todas as informações são preservadas e o estado é reestabelecido, o sistema operacional utiliza uma **tabela de processos**, que é um arranjo de estruturas que guarda essas informações para cada processo.