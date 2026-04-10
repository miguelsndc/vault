$1$ - $a)$
$$\begin{align*}
S&\rightarrow 0\\
S&\rightarrow 0S0\\
S&\rightarrow 0S1\\
S&\rightarrow 1S0\\
S&\rightarrow 1S1\\
\end{align*}$$
$1$ - $b)$
$$\begin{align*}
S &\rightarrow a\\
S &\rightarrow bSa\\
S &\rightarrow aSb\\
S &\rightarrow Sa\\
S &\rightarrow aS\\
S &\rightarrow SS\\
\end{align*}$$

$2)$
Podemos dividir os palíndromos em dois casos: de comprimento par e de comprimento ímpar.

Para palíndromos de comprimento par, que têm a forma ( $ww^{R}$ ): ele lê a primeira parte da palavra empilhando os símbolos. Em algum ponto, de forma não determinística, ele decide que chegou ao meio da palavra e passa a desempilhar, comparando cada símbolo da pilha com o símbolo lido da entrada. A palavra é aceita se ao final da leitura a pilha retorna ao símbolo inicial.

Para palíndromos ímpares, o processo é análogo, exceto que o autômato ao decidir não deterministicamente o ponto do meio, consome um símbolo adicional sem empilhar e então inicia o processo de desempilhamento e comparação.

Por fim, os dois comportamentos podem ser combinados em um único autômato com pilha através de uma transição $\epsilon$ a partir do estado inicial, escolhendo não deterministicamente entre os dois casos.

![[atpilha_palindromo.excalidraw]]
___
$4)$

 ![[Drawing 2026-04-10 16.22.21.excalidraw]]


