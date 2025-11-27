---
tags: compilers
---

Um analisador léxico é um programa que faz parte do front-end de um [[Compiladores|compilador]], é o único do "pipeline" que interage diretamente com o programa fonte, lendo caracter a caracter.

Ele é responsável por ler os caracteres do programa fonte e caracterizar palavras em determinadas categorias previamente definidas, como:
- operadores
- identificadores
- condicionais
- literais, e assim por diante
Existe uma certa hierarquia dentro da análise léxica, no que se refere às palavras que podem ser utilizadas em determinados contextos, existem **palavras reservadas**, como **for**, **if**, **while**, etc, a depender da linguagem. **Não é possível ter uma variável chamada "while" no seu programa**, não é assim que o analisador léxico vai entender.

Para construir uma analisador léxico começa-se a se preocupar com a "microssintaxe" da linguagem, que é nada mais que **o conjunto das regras de separação e agregação de palavras**, ou seja, a **estrutura léxica da linguagem**. 