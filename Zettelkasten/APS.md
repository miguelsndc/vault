
> Nome: **Miguel Santos Nogueira da Costa**

*Em um terminal de comando, liste somente os processos que estão em execução no  terminal atual. Ilustre o resultado obtido*

$1)$ Comando: `ps a`; Resultado obtido:
![[Pasted image 20250718101931.png]]

$2)$ Comando `ps aux` Resultado:

![[Pasted image 20250718102527.png]]

$4)$ Comando `ps -u miguelsndc`; Resultado:

![[Pasted image 20250718102649.png]]

$5)$ Comando utilizado: `pstree`; Resultado:

![[Pasted image 20250718102814.png]]

- $a)$ O processo raiz é o systemd, seu $PID$ é sempre $1$.

- $b)$ Usando `ps -u miguelsndc -o pid,ppid,comm --forest
	 ![[Pasted image 20250718103913.png]]
		Vemos claramento o PID do `ps` $74438$  junto com seu processo pai o `bash`, bem como seu PID $72530$.

- $c)$ Rodando um `sleep` em outro terminal e pegando o $PID$ do bash daquele terminal, eu tenho ![[Pasted image 20250718104533.png]] como árvore, comando `pstree -p <PID>` onde $\rm<PID>$, é o pid do bash.

- $d)$ Comando: `pstree -u miguelsndc`,

![[Pasted image 20250718104919.png]]

Vê se que o usuário iniciou o próprio `systemd` assim como um processo que lida com a interface gráfica, o $\rm gdm$, algo que o gnome usa. 

$6)$ Comando: `top -d 10`; Resultado:

![[Pasted image 20250718112621.png]]

Significado das colunas:
 - **PID**: Identificador do processo.
 - **USER**: Usuário dono do processo
 - **PR**: Prioridade (PR menor tem mais prioridade)
 - **NI**: O valor de "nice", serve para ajuste de prioridade.
 - **VIRT**: Memória virtual total usada.
 - **RES**: Memória residente, (a de fato armazenada na RAM)
 - **SHR**: Memória compartilhada
 - **S**: Estado:
	- S = Sleep
	- R = Running
	- I = Idle
	- Z = Zombie
 - **%CPU**: Percentual de uso da CPU
 - **%MEM**: Percentual de uso da memória RAM
 - **TIME+**: Tempo total de CPU usado pelo processo
 - **COMMAND**: Nome do commando/processo.

$7)$
- $a)$ O comando utilizado foi `cat /proc/<pid>/comm`, as executáveis foram, spotify, gnome-terminal e um componente do firefox em execução.

![[Pasted image 20250718113842.png]]


- $b)$ O comando utilizado foi `cat /proc/<pid>/status` + `grep` para filtrar as informações relevantes à questão, os resultados obtidos estão no print.

![[Pasted image 20250718114150.png]]

- $c)$ TODO

- $d)$ Comandos utilizados `cat /proc/sys/kernel/pid_max` e `cat /proc/sys/kernel/threads-max` Os valores obtidos foram, respectivamente: $4194304$ e $94028$:
![[Pasted image 20250718115002.png]]

$8)$
- $a)$ Executando.
![[Pasted image 20250718121139.png]]

- $b)$ Existem dois identificadores, e eles são diferentes porque cada execução do programa cria um processo diferente no sistema.
- $c)$ A prioridade efetiva e o valor de "Nice" de ambos, é respectivamente $20$ e $0$. 
- $d)$ Ambos pararam de executar e o contador de `stopped` no `top` aumentou em duas unidades, Comando utilizado: `kill -STOP <pid>`

![[Pasted image 20250718121322.png]]

$e)$ O comando utilizado foi `kill -CONT <pid>`; Os processos voltaram a executar e o contador de stopped voltou a ser 0.

![[Pasted image 20250718121145.png]]

$f)$ O Comando utilizado foi: `kill <pid>`,  e ambos os processos sumiram do top.

![[Pasted image 20250718121525.png]]

$g)$ O comando utilizado foi `nice -n 5 ./codigo0`, os resultados obtidos foram:
![[Pasted image 20250718121956.png]]
A prioridade efetiva do `codigo0` aumentou $5$ unidades.

$h)$ O comando utilizado foi `sudo renice -n 15 -p <pid>` 

![[Pasted image 20250718122257.png]]

$j)$ Não foi possível aumentar o valor em mais $10$ unidades, o sistema setou automaticamente a priodade para ser $39$; O comando utilizado foi `sudo renice -n 25 -p <pid>.`


![[Pasted image 20250718122432.png]]


Tentei reduzir a prioridade do processo em execução para -30 com: `renice -n -30 -p <PID>`, o comando não foi aceito como usuário comum:

![[Pasted image 20250718123333.png]]
Em seguida, foi tentada a alteração para nice = 0 como usuário comum: `renice -n 0 -p <PID>`, o comando foi de fato aceito, pois a prioridade não foi aumentada além do permitido.

![[Pasted image 20250718123607.png]]

Após entrar como root:`sudo renice -n -20 -p <PID>`, o comando foi executado e o valor de prioridade foi alterado para $-20$, o menor valor possível e, portanto, a maior prioridade real possível no sistema.

![[Pasted image 20250718123804.png]]

Segue que usuários comuns podem defininir prioridades positivas, e somente o **root** pode definir prioridades mais altas (negativas) para os processos.

$9)$
- $a)$ Foram criados $2$ processos com a execução, os identificadores são: 
![[Pasted image 20250718131012.png]] 
Pai: $87313$ e filho $87314$, a hierarquia é: $87313 \rightarrow 87314$ já que o pai é o $87313$.

- $b)$ O processo pai ainda está rodando por conta do `while(1);` no seu código, o filho termina o seu trabalho após o laço que imprime "Finalizei meu trabalho"  múltiplas vezes.
