
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
