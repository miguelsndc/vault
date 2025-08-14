---
tags: arqcomp
---

Processos são instâncias de um programa em execução, que possuem um espaço de endereçamento lógico, contadores de programa, registradores e variáveis, isto é, entrada, saída e estado. 

> Vale salientar a diferença entre processo e programa, o programa é uma série de instruções modeladas em um ou vários arquivos de código, o processo é a execução desse programa, o programa é a receita, o processo é o preparo.

Vale a pena pensar que por conta da **multiprogramação**, cada processo tem uma CPU **virtual**, embora não seja tecnicamente correto. O computador é capaz de manter vários processos vivos na memória, e a CPU de executar cada um deles por um certo tempo, atualizar os contadores e trocar de processo, existe um certo **pseudo**paralelismo envolvido.

#### Criação de Processos

Em sistemas muito simples, citando o exemplo dos embarcados em microondas por exemplo, é possível ter todos os processos que poderão ser utilizados quando o sistema for ligado. Em sistemas mais complexos, com interação com o usuário, Existem 4 cenários principais para a criação de novos processos:

- Inicialização do Sistema
- Chamadas de sistema por parte de um processo para criação de novos processos filhos
- Solicitação do usuário para criar novo processo.
- Início de uma tarefa em lote *(exclusivo para sistemas em lote)*.

Processos que executam em segundo plano, aguardando algum evento para serem executados, são chamados de **daemons**, alguns exemplos são: o processo que aguarda para notificar a chegada de um novo e-mail, o que está aguardadn

