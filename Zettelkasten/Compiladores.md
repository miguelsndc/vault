---
tags: compiladores
aliases: Introdução
---
>  *O que é uma linguagem e como o computador entende uma linguagem de programação?*

Uma linguagem é um conjunto de símbolos que são atribuídos significado para comunicação, um computador é capaz de entender essa linguagem através de um programa chamado **compilador**, que traduz a linguagem que escrevemos para uma que o computador é capaz de executar.
 
> *O que é um compilador, e o que diferencia um compilador de um interpretador?*

Um compilador é a ferramenta que faz a tradução da linguagem de origem para a linguagem alvo, seja o conjunto de instruções de uma arquitetura de processador ou código de máquina, o compilador é capaz de gerar a linguagem desejada para ser executada. Um interpretador por outro lado recebe tanto o código quanto a entrada, e produz a saída enquanto executa o código. É algo como:

**Compilador**:

Programa $\rightarrow$ **Compilador** $\rightarrow$ Programa Alvo;
Entrada $\rightarrow$ Máquina que executa o Programa Alvo $\rightarrow$ Saída.

**Interpretador**:

Programa e Entrada $\rightarrow$  Interpretador $\rightarrow$ Saída.
 
> *Quais são as fases principais de um compilador e por que a separação em múltiplas etapas é importante?*


>  *Quais princípios fundamentais devem guiar o projeto de um compilador?*

Um compilador deve:
1. *Preservar a intenção do programa compilado* 
2. *Fazer uma otimização discernível do programa compilado*
O primeiro princípio diz respeito à corretude, e é inegociável, se corretude não é estritamente necessária por quê se dar ao trabalho de fazer funcionar ?
E a segunda segue de que os compiladores devem melhorar o programa compilado, seja otimizações de performance inerentes ao processo de compilação, ou melhorias de consumo de energia, latência, disponibilidade por exemplo, portar uma linguagem mais específica para um formato universal.

> *Como os conceitos de compiladores podem ser aplicados em contextos além da construção de compiladores?*

Um compilador é um **microcosmo** da computação, ele possui algoritmos gulosos, de grafo, programação dinâmica, hierarquia de memória, parsing, teoria dos números, sincronização, pipelines, entre outras coisas além de possuir problemas ainda em aberto, é um universo a ser explorado e descoberto.
Ferramentas utilizadas nos compiladores encontram uso em filtros, processamento de texto, busca de textos, buscas na internet, pattern matching, etc.

#### Estrutura de um Compilador

Um compilador tem duas tarefas, entender a linguagem fonte e mapear suas semântica pra linguagem alvo. Naturalmente, existe uma divisão do trabalho associado a essas duas tarefas, o **front-end**, que cuida do *entender* e o **back-end** que cuida do *mapear*.

O front-end codifica o seu retorno em um formato que o back-end pode entender e utilizar, o back pode assumir que este formato é livre de erros, dado que a checagem é feita pelo front. Esta representação 
