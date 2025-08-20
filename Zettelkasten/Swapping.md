---
tags: arqcomp
---

Geralmente a necessidade de memória de todos os processos em execução é bem maior do que a memória ram disponível, portanto, estratégias foram criadas para sanar esse problema, o **Swapping**, que veremos aqui e a [[Memória Virtual]], que é outra forma de se alcançar o mesmo objetivo.

Com o swapping, processos inteiros são movidos entre disco e memória, de tal forma que processos "inativos" são movidos para o disco, enquanto processos que estão sendo executados são trazidos para a memória, executados por um tempo, e mandados de volta pro disco.

Se os processos forem estáticos, isto é, necessitem da mesma quantidade de memória, de criação até a sua morte, então é simples **gerenciar os espaços de cada processo**, basta alocar exatamente o que cada processo precisa. Porém, a alocação dinâmica é o mais comum, então precisamos de uma forma de gerenciar o **crescimento dos processos (ou encolhimento)**,
