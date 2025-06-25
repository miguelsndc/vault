### Tópico 1

**Arquitetura:** Se refere aos atributos que são visíveis ao programador, que tem impacto direto na execução lógica do programa.
**Organização**: Refere-se as unidades operacionais que implementam a arquitetura.
**Memória**:
- Principal: É a memória RAM, volátil e mais rápida que as secundárias
- Secundária: Mais lentas e mais baratas, boas para armazenamento massivo de dados.
**Cache**: pequenas memórias próximas ao processador para armazenar **parte** dos dados e programas da memória principal (RAM), evita barramento e torna o acesso mais rápido (SRAM)

**Desempenho**
- Tempo de resposta: tempo necessário para completar uma tarefa.
- **Throughput**: Total de trabalho realizado por unidade de tempo (tasks/hora, etc.)

Como medir desempenho? 
$$\begin{align*}
\text{Performance}_{x}&= \frac{1}{\text{Execution Time}_{x}} 
\end{align*}$$
Então se $$\begin{align*}
Performance_{x}> Performance_{y}\\
\frac{1}{Execution Time}_{x}>\frac{1}{Execution Time}_{y}\\
ExecutionTime_{y}>ExecutionTime_{x}
\end{align*}$$
Então $x$ roda mais rápido que $y$.
**Como relacionar o desempenho de diferentes computadores quantitativamente ?**
- $X$ é $n$ vezes mais rápido que $Y$:
$$\begin{align*}
\frac{Perfomance_{X}}{Performance_{Y}}=n
\end{align*}$$
- Se $X$ é n vezes mais rápido que $Y$, então o tempo de execução de $Y$ é n vezes maior que $X$:
$$\begin{align*}
\frac{ExecutionTime_{Y}}{ExecutionTime_{X}}=n
\end{align*}$$ 
**Frequência de Clock é o inverso do período de clock**.
**Uma métrica simples de desempenho de CPU é**:
$$\begin{align*}
CpuExecutionTime &= CpuClockCycles \times ClockCycleTime \\
CpuExecutionTime &= \frac{CpuClockCycles}{ClockRate} 
\end{align*}$$
O desempenho pode ser melhorado:
- Reduzindo o número de ciclos
- Reduzir o tamanho do ciclo (Aumentando a Frequência)
- avaliar freq x n de ciclos.

Outra métrica:

**O Tempo de execução deve depender do número de instruções geradas pelo compilador**:
- o número de ciclos de clock para exec. do programa pode ser dado:
	- $CpuClockCycles = InstructionsForProgram \times AverageClockCyclesPerInstruction$;
- **CPI** (Número de ciclos médio por instrução).
	- é a média do número de ciclos de todas as instruções executadas no programa.

- Tempo de ciclo = $\tau = \frac{1}{f}$ onde $f$ é a frequência constante do processador
$$\begin{align*}
CPI &= \frac{\sum\limits_{i=1}^{n}CPI_{i}\times I_{i}}{ I}
\end{align*}$$
Então o tempo para executar um programa é $T = I \times CPI \times \tau$ 

Coisas para levar desse Tópico:

**Taxas MIPS/MFLOPS** 

- MIPS é uma métrica de **milhões de instruções por segundo**.
- $T \times MIPS = \frac{I}{T\times 10^{6}} = \frac{f}{CPI \times 10^{6}}$ (Se chega na segunda fórmula substituindo $T$ na primeira.)
	- Derivação útil: $I=T×MIPS×10^{6}$ 
- MFLOPS é voltada para operações de ponto flutuante, sendo:
	- $MFLOPS = \frac{\text{Numero de operacoes de ponto flutuante executadas no programa}}{\text{Tempo de execução} \times 10^{6}}$ 

**Lei de Amdahl**
$$\begin{align*}
\text{Tempo de execução após melhoria} &= \frac{\text{Tempo de execução afetado pela melhoria}}{\text{Qtd de Melhoria}} + \text{Tempo não afetado pela melhoria}
\end{align*}$$

• Considere um programa rodando em um único processador, de modo que:
	• Um fração $(1 – f)$ do tempo de execução envolva um código serial
	• Uma fracão $f$ envolva código infinitamente paralelizável sem overhead de escalonamento

Então o speedup obtido explorando a parte paralela com $N$ processadores paralelos é: $$\begin{align*}
\frac{T(1-f) + Tf}{(1-f)+  \frac{Tf}{N}}&= \frac{1}{(1-f) + \frac{f}{N}}
\end{align*}$$
Quando $N$ tende ao infinito, o speedup é limitado a $\frac{1}{1-f}$.


**Medir tempo de execução de um programa**
- $T = I \times CPI \times \tau = \frac{I \times CPI}{f}$ 
	- $T$ = Tempo de execução
	- $I$ = Número de instruções totais do programa
	- $CPI$ = média de quantos ciclos de clock são necessários para executar uma instrução
	- $CPI = \frac{\sum\limits_{i=1}^{n}CPI_{i}\times I_{i}}{I}$ , sendo cada $CPI_{i}$ fornecido pela arquitetura, $I_{i}$ a quantidade de intruções, e o $I$ a soma de todas as instruções.
	- $\frac{Performance_{A}}{Performance_{B}}= \frac{ExecutionTime_{B}}{ExecutionTime_{A}=}= x$ onde $T_{A}= x * T_{B}$, A roda $x$ vezes mais rápido que $B$.
	- $\text{CPU Clock Cycles}$ = $I \times CPI$.
	- Speedup = $$\begin{align*}
\frac{\text{Des. após da melhoria}}{\text{Des. antes melhoria}} &= \frac{\text{Tempo de execução antes melhoria}}{\text{Tempo de execução após melhoria} }
\end{align*}$$
		Ou seja, se um recurso for usado por uma fração $f$ do tempo antes de **melhoria** e a quantidade e melhoria seja $N_{f}$, Speedup = $$\begin{align*}
Speedup &= \frac{1}{(1-f) + \frac{f}{N_{f}}}
\end{align*}$$

___
### Tópico 3

**DRAM (Dynamic Random Access Memory)**
- Maior tempo de acesso
- Necessita de refreshing
- Baixo custo por bit
**SRAM (Static Random Access Memory)**
- Pequeno tempo de acesso
- Não existe refreshing
- Alto custo por bit
- Cache.

##### Princípio da Localidade:
- **Localidade Temporal**: 
	- Programa tende a referenciar instruções e dados referenciados recentemente!
	- Mantenha itens mais recentemente referenciados junto ao processador, como instruções de um loop.
- **Localidade Espacial**: 
	- Programa tende a referenciar instruções e dados que tenham endereços próximos das últimas referências.
	- Mova blocos de dados de palavras contíguas para junto do processador, como dados de um vetor.

##### Hierarquia de memória

**Componentes ordenados por custo, tamanho . Velocidade (maior pra menor)**
1. CPU e Cache L1
2. Cache L2
3. Memória principal (RAM)
4. Memória Secundária (Disco)

**Terminologias**:
- **Bloco (linha)**: unidade mínima de informação presente numa hierarquia de memória.
- **Hit**: Ocorre quando os dados requisitados pela CPU estão em algum bloco do nível de memória desejado
- **Miss**: Ocorre quando os dados **não** estão em algum bloco de nível desejado e é necessário buscar em um nível inferior e transferir pra cima.
- **Miss Penalty**: o tempo que leva para buscar o bloco de um nível abaixo para um nível mais acima e enviar para a CPU.

**Mapeamento Direto**

Para saber se um item está na cache, utiliza-se bastante a função módulo, isto é $(\text{endereço do bloco na memoria})\;\; mod \;\;(\text{número de blocos na cache})$. como módulo não é injetiva, precisa-se distinguir se a palavra na posição da cache é a esperada, pra isso usa-se um **conjunto de tags** **(tag field)**:
 -  Bits mais significativos do endereço de memória não utilizados para determinar o índice do cache. Por exemplo, se houverem 64 posições na cache, utiliza-se os 6 primeiros bits do endereço e os outros para diferenciar.

> Informações na cache podem não estar válidas, por isso se utiliza uma tag de validade.

Índice do bloco da cache se encontra com:

$$\begin{align*}
\left(\bigg\lfloor\frac{\text{Byte adress}}{\text{Bytes per block}}\bigg\rfloor\right) \mod \text{qtd blocos}
\end{align*}$$
##### Escrita
Existem duas formas de lidar com escrita na memória:
- **Write-Through**: Escreve ao mesmo tempo no cache e na memória
	- Nega a ideia de se evitar escrever na memória principal, a perda de desempenho é significativa
	- Pode-se guardar um buffer para postergar as mudanças somente quando o buffer estiver cheio, então, stalla o processador e aplica as mudanças
- **Write-Back**: Escreve somente na cache, então quando o bloco modificado é removido da cache ele é escrito na memória principal.
	- Cada bloco da cache precisa de um **dirty bit**, que indica se o valor precisa ou não ser salvo na memória antes de reescrito.

##### Desempenho da cache
$$\begin{align*}
CpuTime &= (CpuExecutionClockCycles + MemoryStallClockCycles) \times ClockCycleTime\\
\end{align*}$$
Simplificando:
$$\begin{align*}
MemoryStallClockCycle&= \frac{Instructions}{Program}\times \frac{Misses}{Instruction} \times Miss Penalty
\end{align*}$$
**AMAT**: métrica para capturar o tempo de acesso a memória considerando ambos hit e miss:
- $HitTime + (MissRate \times MissPenalty)$.
