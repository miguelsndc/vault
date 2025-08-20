---
tags: arqcomp
---

A memória que pode ser mantida em [[Mapas de bits]] também pode ser mantida por listas encadeadas **ordenadas pelos endereços**, que mantém nós que dizem se:
- Está ocupado ou não
- Qual os endereços livres (começo + bloco, semelhante à [[Registradores Base e Limite]]).
- Ponteiros para o próximo bloco.
Este método tem a vantagem de possibilitar vários algoritmos para encontrar um espaço para alocar um processo, e também a desalocação de memória quando um processo termina é dividida em 4 casos:

![[Pasted image 20250820190502.png]]

O que talvez torne mais conveniente manter uma lista duplamente encadeada para facilitar o caso $c)$.

#### Algoritmos de achar o espaço livre

Como as listas são ordenadas pelos endereços, vários algoritmos para encontrar espaços livres para alocar processos são possíveis, dentre eles:

- **First fit**: o algoritmo mais simples e mais rápido, simplesmente aloca a memória no primeiro espaço que couber.
- **Best-fit**: Aloca o processo mo espaço mais "apertado", precisa buscar na lista inteira.
- **Worst-fit**: Aloca o processo no maior espaço disponível, busca a lista inteira.
- **Next-fit**: Semelhante ao first-fit, porém memoriza o espaço que encontrou na ultima busca, e busca a partir dela na próxima alocação.

