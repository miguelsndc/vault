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

$5)$ Esconde-se as rotinas críticas do sistema operacional por trás de um modo especial, para que nem todo processo tenha acesso a 100% do hardware do computador, por questões de segurança, privacidade, integridade e desempenho, essas rotinas são devidamente escondidas e cuidadosamente verifica-se as chamadas de sistema para garantir o bom funcionamento. Além do mais, a maioria das funções desempenhadas por programas de usuário não necessitam de operações absurdas do sistema, geralmente IO e E/S, que são devidamente 