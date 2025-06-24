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
	- Derivação útil: "$I=T×MIPS×10^{6}$" 
- MFLOPS é voltada para operações de ponto flutuante, sendo:
	- $MFLOPS = \frac{\text{Numero de operacoes de ponto flutuante executadas no programa}}{\text{Tempo de execução} \times 10^{6}}$ 

**Lei de Amdahl**
$$\begin{align*}
\text{Tempo de execução após melhoria} &= \frac{\text{Tempo de execução afetado pela melhoria}}{\text{Qtd de Melhoria}} + \text{Tempo não afetado pela melhoria}
\end{align*}$$



**Medir tempo de execução de um programa**
- $T = I \times CPI \times \tau = \frac{I \times CPI}{f}$ 
	- $T$ = Tempo de execução
	- $I$ = Número de instruções totais do programa
	- $CPI$ = média de quantos ciclos de clock são necessários para executar uma instrução
	- $CPI = \frac{\sum\limits_{i=1}^{n}CPI_{i}\times I_{i}}{I}$ , sendo cada $CPI_{i}$ fornecido pela arquitetura, $I_{i}$ a quantidade de intruções, e o $I$ a soma de todas as instruções.
	- $\frac{Performance_{A}}{Performance_{B}}= \frac{ExecutionTime_{B}}{ExecutionTime_{A}=}= x$ onde $T_{A}= x * T_{B}$, A roda $x$ vezes mais rápido que $B$.
	- $\text{CPU Clock Cycles}$ = $I \times CPI$.