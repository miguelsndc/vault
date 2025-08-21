---
tags: arqcomp
---
Embora hajam boas estratégias para gerenciamento de memória, como [[Swapping]] e os úteis [[Registradores Base e Limite]], ainda é preciso lidar com **bloatware**, *(programas que excedem o tamanho da memória disponível)*. Uma solução dada foi a **memória virtual**, que divide o [[Espaço de Endereçamento]] de um processo em blocos chamados **páginas**, que são **blocos contíguos de endereços** que são mapeados para a memória fisica mas nem todas as páginas precisam estar em memória ao mesmo tempo.
Caso o processo referencie um endereço que faz parte de uma página que esteja em memória física, o hardware rapidamente faz o mapeamento. Caso não, o sistema operacional é alertado para ir buscar a página que falta e reexecuta a instrução que falhou.


#### Paginação

Quando um processo referencia um endereço de memória, em uma instrução, esses endereços podem ser gerados por diversos métodos, por exemplo, [[Registradores Base e Limite]]. Esses endereços gerados são chamados de **endereços virtuais** e foram o **espaço de endereçamento virtual**, em computadores sem memória virtual, o endereço gerado é colocado diretamente no barramento de memória e faz com que a palavra física com o mesmo endereço seja escrita ou lida. Quando o computador possui esquema de **memória virtual**, os endereços antes passam pela ***MMU (Memory Management Unit)***, que vai mapear os endereços virtuais em endereços físicos.

O espaço de endereçamento virtual consiste em blocos de tamanho fixo chamados **páginas**, esses blocos que estão presentes na memória física são chamados de **quadros de páginas**, geralmente eles tem o mesmo tamanho.

As páginas são marcadas com um bit de presença que indica se elas estão na memória física ou não no mapa da MMU. Quando um endereço presente em uma página que não está em memória é referenciado, a MMU interrompe e desvia pro sistema operacional, isso se chama **page fault (falta de página)** e então uma rotina de:
- Escolher um quadro de página para mandar pro disco.
- Carrega do disco a página referenciada no quadro de página recém-liberado
		> Se o sistema operacional escolher a página 1 para ser substituída por exemplo, primeiro o SO marca a página 1 como não mapeada para evitar acessos nesse meio tempo, então marca o bit de presença na página que entrou.
- Reinicia a instrução que falhou.

#### Tabelas de Páginas

**Implementação simples**

O mapeamento de endereços virtuais para físicos é feito da seguinte forma: com um endereço de 16 bits por exemplo, e páginas de 4KB, os 4 bits mais significativos poderiam especificar uma das 16 páginas, e os outros 12 bits especificariam então o deslocamento dentro dessa página. 
Então, o número da página virtual é usado como índice na tabela de páginas, que vai dar o número do quadro de páginas físico, onde está armazenado na RAM, (caso esteja, se não, desvia pro SO e aguarda),  agora, substitui-se os 4 msb's pelo número do quadro físico. Tendo o número do quadro e o offset fica fácil mandar pro barramento ler/escrever a memória.

**Estrutura de uma Entrada de Tabela de Página**

O campo mais importante de uma tabela de página é o número do quadro de página, já que é ele que se deseja localizar, mas também há outras informações importantes:
- Bit de presente na memória ou não.
- Bits de proteção que dizem quais tipos de acesso são permitidos, podem ser até 3 bits para leitura / escrita / execução.
- Bit de *modificada* ou **dirty bit**: É um bit que indica que uma página foi alterada, e caso o sistema operacional deseje recuperar um quadro de página e a página dentro do quadro foi alterada (isto é, está "suja"), ela também precisa ser alterada no disco, se não foi, ela pode ser abandonada, tendo em vista que a cópia em disco ainda é válida.
- Bit de *referenciada*: É o bit que o sistema operacional usa para saber quais páginas foram referenciadas recentemente, e ajuda o sistema operacional a escolher um quadro de página para ser substituído.


#### Translation Lookaside Buffer

Pesquisadores perceberam que uma fração pequena das páginas são recorrentemente referenciadas, e que existem várias página que sequer são encostadas, por isso, um pedaço especial de hardware foi criado, o **Translation Lookaside Buffer**, que é como se fosse um cache para páginas, que inclui informações semelhantes à tabela de páginas, mas por possuir hardware dedicado é muito mais rápido, é evidente que age como um **"middle-man"** na frente da tabela de páginas, dentro da MMU, é importante destacar que ele sempre é atualizado para conter as páginas mais recentemente referenciadas.

o TLB introduz alguns novos conceitos, especialmente sobre **page faults**
-  **Soft-miss**: quando a página não está no TLB mas está na memória, e basta que a TLB seja atualizada.
- **Hard-miss**: Quando a página em si não está na memória e precisa ser carregada do disco.
- **Minor page fault**: A página está na memória, e pode ter sido trazida do disco por outro processo, então basta fazer os paranauê na tabela para funcionar.
- **Major page fault**: Precisa ser trazida do disco.
- **Segmentation Fault**: Um endereço inválido foi referenciado e nenhum mapeamento precisa ser acrescentado ao TLB