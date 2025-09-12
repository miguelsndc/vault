---
tags: compiladores, review
---
#### Analisador Léxico

O papel de um analisador léxico é ler uma stream de caracteres e os transformar em uma stream de palavras da linguagem, assinalando a cada palavra uma categoria sintática, para alcançar essa agregação e classificação, o analisador léxico aplica um conjunto de regras que define a estrutura léxica da linguagem, também chamada de **microssintaxe** da linguagem.

A **Microssintaxe** de uma linguagem é uma definição que diz como separar caracteres em palavras e como separar as palavras entre si, é importante salientar que palavras que dão match com **identificadores** *(o nome utilizado para se referir a variáveis)*, podem ter categorias sintáticas diferentes dado que podem ser **palavras reservadas**, **keywords**, como `while` ou `static`, e por isso não são passíveis de uso para outro fim. O analisador pode utilizar um dicionário para checar a disponibilidade da palavra usada ou a incluir na sua microssintaxe.


