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


Seja B a linguagem de todos os palı́ndromos sobre {0, 1} contendo o mesmo número de 0s e 1s.
Mostre que B não é livre de contexto.


- o palindromo tem que ser par
- 0000 1100111 nao vai
- tem que ser 01S10 
- 10S01
- S -> 10S01 | 01S10 | $\epsilon$ 
- 1010 0101
- 101010 010101
- $(10)^{n} (01)^{n}$ 


Suponha, por contradição, que B seja uma linguagem livre de contexto. Seja $p≥1$ o comprimento do bombeamento associado a B.
Considere a palavra $s \in B$ definida por:
$$\begin{align*}
s=0^{p}1^{2p}0^{p}
\end{align*}$$Note que $∣s∣=4p≥p$, $s$ é um palíndromo e possui exatos $2p$ zeros e $2p$ uns.

Pelo Lema do Bombeamento, existe uma divisão de $s$ na forma s=$uvxyz$ que satisfaz:
- $∣vy∣≥1$ : pelo menos uma parte a ser bombeada não é vazia
- $∣vxy∣≤p$ : a janela de bombeamento é limitada pelo tamanho $p$
- Para todo $i≥0$, $uvixyiz\in B$

Como o tamanho máximo da janela $∣vxy∣$ é $p$, a substring $vxy$ não pode abranger simultaneamente o primeiro bloco de zeros (0p) e o último bloco de zeros (0p), pois eles estão separados por 2p uns. Portanto, vxy deve se enquadrar em uma das três posições abaixo. Avaliaremos o bombeamento para i=2 (a palavra uv2xy2z):
 
 **Caso 1: vxy está contido estritamente no bloco inicial 0p ou estritamente no bloco final 0p.** Ao bombear (i=2), adicionaremos zeros em apenas uma das extremidades da palavra. A palavra resultante perderá a simetria estrutural e não será mais lida da mesma forma nos dois sentidos. Logo, uv2xy2z deixa de ser um palíndromo, o que implica uv2xy2z∈/B.

**Caso 2: vxy está contido estritamente no bloco central 12p.** Ao bombear (i=2), adicionaremos apenas caracteres 1. A palavra resultante terá mais uns do que zeros (pois a quantidade de zeros permaneceu a mesma). Faltando o balanço quantitativo, uv2xy2z∈/B.

 **Caso 3: vxy sobrepõe a fronteira entre 0p e 12p, ou entre 12p e 0p.** Neste caso, os elementos v e y contêm zeros do bloco inicial (ou final) e/ou uns do bloco central. Ao bombear (i=2), a quantidade de zeros aumentará de forma assimétrica em relação ao centro da palavra, destruindo a propriedade de palíndromo. Adicionalmente, pode quebrar a paridade entre zeros e uns. Portanto, uv2xy2z∈/B.

**Conclusão:** Em todos os cenários possíveis delimitados pela condição ∣vxy∣≤p, existe um i (no caso, i=2) tal que uvixyiz∈/B. Isso é uma contradição direta com a condição **(iii)** do Lema do Bombeamento.

Logo, a premissa inicial é falsa. Conclui-se rigorosamente que B não é uma linguagem livre de contexto. ■











