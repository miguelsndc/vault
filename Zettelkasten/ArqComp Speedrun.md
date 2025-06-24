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
