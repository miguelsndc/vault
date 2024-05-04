$1)$ 
$a)$ Assumindo que todas as bolas tem a mesma probabilidade de serem escolhidas, A probabilidade de escolher a primeira bola preta é $\frac{6}{11}$, a segunda $\frac{1}{2}$, e a terceira $\frac{1}{3}$, dado que não há reposição, então a probabilidade é $\frac{6}{11}\cdot \frac{1}{2}\cdot \frac{1}{3}= 0.09$.
$b)$ A probabilidade de escolher uma bola branca numa urna cheia é $\frac{5}{11}$, A probabilidade de **não** escolher uma bola branca, supondo que a primeira foi escolhida, e que a ordem não importa, é de $1 - \frac{4}{10} = \frac{6}{10}$ e $1 - \frac{4}{9}=\frac{5}{9}$, então a probabilidade é $\frac{5}{11} * \frac{6}{10} * \frac{5}{9} = 0.15$.
$c)$ A probabilidade de todas as bolas serem pretas foi discutida na alternativa $a)$, para que **pelo menos uma** das bolas sejam pretas, basta encontrar a probabilidade do evento complementar de $a)$, sendo este $1 - 0.09 = 0.91$.

$2)$ 
$a)$ Dado que há $270$ alunos no total e $90$ alunos de S.I, a probabilidade é $p(SI)=0.33$. 
$b)$ $p(CC_{linkedin})= \frac{28}{90}= 0.31$. Dado que, de $90$ alunos de $CC$, $28$ preferem o linkedin.
$c)$ A probabilidade de um aluno de EC preferir o $X$ é dado por $p(EC_{X})=\frac{1}{10}$, os que **não** preferem o $X$ é dada por $p(EC_{X}^{c})=1- \frac{1}{10}= \frac{9}{10}=0.9$. 

$4)$ Seja $A$ o evento que denota uma peça da caixa $A$ ser defeituosa, e $B$ o evento que denota uma peça da caixa $B$ ser defeituosa. Temos de antemão que 3 de $A$ são defeituosas e $2$ de $B$ também. Podemos dizer que $p(A) = \frac{3}{8}$ e $p(B) = \frac{2}{5}$.

$a)$ A probabilidade de $A$ não ser defeituosa é dada por $p(A^{c})$ e de $B$ não ser defeituosa é dada por $p(B^{c})$. a probabilidade de ambas não serem defeituosas é dada por $p(A^{c} \cap B^{c})=\frac{5}{8}\cdot \frac{3}{5}= 0.37$. 

$b)$ Como não foi especificada de qual caixa a peça viria defeituosa ou não, faremos assim:
A probabilidade de $A$ vir defeituosa é dada por $p(A\cap B^{c})$ e de $B$ vir defeituosa é dada por $p(A^{c}\cap B)$, logo temos:
$$\begin{align*}
p((A \cap B^{c}) \cup (A^{c} \cap B))=p(A \cap B^{c}) + p(A^{c}\cap B) - (A\cap B^{c} \cap A^{c} \cap B^{c})\\

\end{align*}$$
O último termo é vazio. logo temos:
$$\begin{align*}
p((A \cap B^{c}) \cup (A^{c} \cap B)) &= \left(\frac{3}{8} \cdot \frac{3}{5}\right)+ \left(\frac{5}{8} \cdot \frac{2}{5}\right)= 0.47
\end{align*}$$
Que é a probabilidade de uma peça de uma caixa vir defeituosa e outra não.

$c)$ Dado que uma peça é defeituosa e outra não, sendo $C$ esse evento, como dito anteriormente, $p(C) = 0.47$, a probabilidade que ela venha de $A$ é dada por:
$$\begin{align*}
p(A\mid C) &= \frac{p(C \mid A)p(A)}{p(C)}
\end{align*}$$
sabemos que $p(A) = \frac{3}{8}$ e $p(C) = 0.47$, $p(C\mid A)= \frac{p(A \cap C)}{P(A)}$, $p(A\cap C) = 0.37 \cdot 0.47 = 0.17$, logo $p(C \mid A) = \frac{0.17}{0.37}= 0.45$, e portanto $p(A \mid C) = \frac{0.45 \cdot 0.37}{0.47}= 0.35$.    
