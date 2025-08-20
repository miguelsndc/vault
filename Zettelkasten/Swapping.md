---
tags: arqcomp
---

Geralmente a necessidade de memória de todos os processos em execução é bem maior do que a memória ram disponível, portanto, estratégias foram criadas para sanar esse problema, o **Swapping**, que veremos aqui e a [[Memória Virtual]], que é outra forma de se alcançar o mesmo objetivo.

Com o swapping, processos inteiros são movidos entre disco e memória, de tal forma que processos "inativos" são movidos para o disco, enquanto processos que estão sendo executados são trazidos para a memória, executados por um tempo, e mandados de volta pro disco.

Se os processos forem estáticos, isto é, necessitem da mesma quantidade de memória, de criação até a sua morte, então é simples **gerenciar os espaços de cada processo**, basta alocar exatamente o que cada processo precisa. Porém, a alocação dinâmica é o mais comum. Soa como uma boa ideia alocar um pouco mais de memória do que o processo precisa naquele ponto no tempo, para evitar mover incessantemente processos de lugar de tal forma que haja espaço para todos. É válido notar que mover esse **espaço livre** para o disco é desperdício, então movemos apenas o que é usado pelo processo, porém, precisamos de uma forma de gerenciar esse **crescimento dos processos (ou encolhimento)**, e essa **memória livre**, entre soluções temos [[Mapas de bits]] ou [[Listas Livres]]. 
