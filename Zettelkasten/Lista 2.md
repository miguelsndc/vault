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

Como o tamanho máximo da janela $∣vxy∣$ é $p$, a substring $vxy$ não pode abranger simultaneamente o primeiro bloco de zeros ($0p$) e o último bloco de zeros ($0p$), pois eles estão separados por $2p$ uns. Portanto, $vxy$ deve se enquadrar em um dos três casos abaixo. Vamos avaliar o bombeamento para $i=2$ (a palavra $uv^{2}xy^{2}z$):
 
 1. $vxy$ está contido estritamente no bloco inicial $0p$ ou estritamente no bloco final $0p$. Ao bombear adicionaremos zeros em apenas uma das extremidades da palavra. A palavra resultante perderá a simetria. Logo, $uv^{2}xy^{2}z$ deixa de ser um palíndromo, o que implica $uv^{2}xy^{2}z \notin B.$

2. $vxy$ está contido estritamente no bloco central $1^{2p}$ . Ao bombear, adicionaremos apenas caracteres 1. A palavra resultante terá mais uns do que zeros. Portanto $uv^{2}xy^{2}z \notin B$.

3. $vxy$ está entre $0^{p}$ e $1^{2p}$, ou entre $1^{2p}$e $0^{p}$. Neste caso, os elementos $v$ e $y$ contêm zeros do bloco inicial (ou final) e/ou uns do bloco central. Ao bombear, a quantidade de zeros aumentará de forma assimétrica em relação ao centro da palavra, destruindo a propriedade de palíndromo. Adicionalmente, pode quebrar a paridade entre zeros e uns. Portanto, $uv^{2}xy^{2}z \notin B$.

Em todos os cenários possíveis existe um $i$ tal que $uv^{i}xy^{i}z \notin B$. Isso quebra a condição $3$ do lema do bombeamento, logo, temos uma contradição, e $B$ não é livre de contexto.











