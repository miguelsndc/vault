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

Para construir uma analisador léxico começa-se a se preocupar com a "microssintaxe" da linguagem, que é nada mais que **o conjunto das regras de separação e agregação de palavras**, ou seja, a **estrutura léxica da linguagem**. Temos:

1. **Token**: que são as categorias léxicas da linguagem, um par com o nome e atributos adicionais.
2. **Padrão**: descrição dos possíveis *lexemas* associados a um token, isto é, um "blueprint" das características que uma palavra precisa satisfazer para ser designado à um tipo específico de token.
3. **Lexema**: É a sequência de caracteres que casam com o tipo de Token, o "valor" de fato da palavra.

Por exemplo: 
`var1 = 23;`
Para o Token: `Token<ID, "var1">` 
- Padrão: *sequência de caracteres seguidos por dígitos*
- Lexema: "var1".
- ID: Tipo do Token.