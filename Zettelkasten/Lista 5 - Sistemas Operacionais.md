---
tags: arqcomp
---

$1)$ As duas principais funções de um sistema operacional é realizar as operações complexas exigidas pelo hardware no lugar do programador, e oferecer uma interface que abstraia essas tarefas complexas para algo mais simples.

$2)$ Se não houver isolamento adequado, um usuário pode ter acesso a informações sensíveis de processos sendo executados por outros usuários, como também pode inferir dados observando recursos compartilhados, como cache, disco, etc.

$3)$ Instruções privilegiadas podem ser executadas somente no modo núcleo do processador, sendo necessário uma interrupção para chavear pro modo núcleo, ou uma chamada de sistema, para que seja executada, instruções não privilegiadas podem ser executadas em modo usuário.

$4)$ Porque dispositivos de E/S lidam diretamente com hardware e são sensíveis, pode-se:
- Comprometer a integridade do sistema ao realizar uma sobrescrever dados em disco, corrompendo arquivos e até mesmo ou travar dispositivos.
- Pode-se comprometer os próprios dispositivos, por exemplo, movimentação do cabeçote em um disco pode causar desgaste prematuro e/ou comprometer seu funcionamento
- Violar segurança e privacidade ao ter acesso irrestrito à câmeras, teclados, mouses, etc.

$5)$ Esconde-se as rotinas críticas do sistema operacional por trás de um modo especial, para que nem todo processo tenha acesso a 100% do hardware do computador, por questões de segurança, privacidade, integridade e desempenho, essas rotinas são devidamente escondidas e cuidadosamente verifica-se as chamadas de sistema para garantir o bom funcionamento. Além do mais, a maioria das funções desempenhadas por programas de usuário não necessitam de operações absurdas do sistema, geralmente IO e E/S, que são devidamente handled através de chamadas de sistema.

$6)$ a,d,e,f,

$7)$ A arquitetura monolítica não esconde nada de ninguém, todas as rotinas estão visíveis para todas as outras, trazendo simplicidade, e eficiência, a custo de um sistema díficil de lidar e compreender, além do mais, quaisquer processo que quebre compromente o sistema inteiro, pois pode facilmente, por exemplo, referenciar um endereço de memória inválido.

A arquitetura em camadas tenta dividir as funções do sistema em, bom, camadas, onde o nível de profundidamente das camadas diz o quão interno são suas responsabilidades, e camadas se comunicam por chamadas de sistema, existe uma clara vantagem de organização e compreensão deste tipo de sistema, porém o overhead de comunicação entre as camadas é uma desvantagem clara.


$8)$ A arquitetura de microkernel se desenvolve a partir da ideia de que o núcleo pode e deve ser mínimo, para trazer confiabilidade e resiliência ao sistema, dado que erros no núcleo são absolutamente críticos e compremetem todo o sistema operacional, e erros em processos de usuários podem ser resolvidos simplesmente matando o processo defeituoso, a arquitetura de micro-kernel se divide em:

- Micronúcleo: responsável por chavear processos, gerenciar dispositivos de E/S, gerenciar memória, e demais operações de modo núcleo.
- Servidores, que implementam funções do SO como processos de usuário, temos por exemplo, o servidor de rede, de impressão, de arquivos, de memória, que fazem chamadas ao núcleo, que responde devidamente, fornecendo basicamente uma comunicação entre os processos

Vantagens são: Facilidade de depuração, manutenção, gerenciamento.
Como desvantagem podemos citar: desempenho, dado que cada comunicação entre cliente-servidor, temos uma troca do modo de acesso, (núcleo envolvido).

$9)$ System calls ou chamadas para o sistema são rotinas invocadas por processos em modo usuário que desejam acessar um recurso ou executar uma ação que está protegida pelo sistema operacional e pode somente ser executada em modo núcleo. Um processo que faz uma chamada de sistema passa o controle para o sistema operacional, que cuidadosamente avalia a chamada para garantir consistência e corretude dos parâmetros, que então a executa com segurança e devolve o controle à instrução seguinte do processo, chamadas de sistema são abstrações que garantem a segurança, desempenho e confiabilidade do sistema, abstraindo de processos de usuário funções que não os cabem.

$10)$ Todos os processos tem um espaço de endereçamento virtual/lógico onde pode trabalhar, o que simplifica o desenvolvimento e traz mais segurança, já que ter vários processos trabalhando com endereços físicos é garantia de problemas. Além disso o sistema operacional pode mover processos de lugar na memória sem que o processo falhe, já que todo o mapeamento para endereços físicos é feito por ele.