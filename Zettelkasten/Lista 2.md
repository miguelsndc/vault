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
$2)$ Podemos dividir em dois casos:
- Palíndromos pares
- Palíndromos ímpares
E resolver cada caso separadamente, e então unir os dois autômatos resultantes.
Os palíndromos pares caem no caso $ww^{R}$, que pode ser resolvido com o autômato construído em sala: empilha os caracteres de $w$ e transiciona não-deterministicamente para desempilhá-los em seguida, "chutando", onde acontece a quebra entre $w$ e $w^{R}$, se a pilha estiver vazia, aceite.

Os palíndromos pares são análogos, porém há um símbolo $x$ no meio, que deve ser ignorado
