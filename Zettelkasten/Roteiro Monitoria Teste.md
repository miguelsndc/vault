Duração: Aproximadamente $30$ minutos
Plano inicial:
- Introduzir Matrizes Ortogonais e Simétricas (3 minutos)
	- Definição
	- Propriedades
- Operadores Ortogonais (8 minutos)
	- Definição
	- Propriedades
- Operadores Auto-adjuntos (8 minutos)
	- Definição
	- Propriedades
	- Teorema Espectral 
- Resolver a Questão (5 minutos)
___
Matrizes Ortogonais - Definição:
Uma matriz $A$ é dita *ortogonal* se:
- $A \cdot A^{T}=I$, ou seja, a inversa de $A$ é $A^{T}$
Uma matriz $B$ é dita simétrica se $B = B^{T}$, isto é $b_{ij}=b_{ji}$, os escalares são refletidos através da diagonal principal.

Exemplos de Matrizes Ortogonais:
- Rotação no $R^{2}$ e $R^{3}$

Seja $A$ uma matriz ortogonal, então $\det{A} = \pm 1$.
$$
\begin{align*}
A \cdot A^{T}&= I\\
\det(A\cdot A^{T})&= \det(I)\\
\det(A)\cdot \det(A^{T})&= 1\\
(\det(A))^{2}&= 1\\
\det(A) &= \pm 1
\end{align*}
$$
Uma matriz $A$ é ortogonal em se e somente se, com relação a alguma base $\alpha$, os vetores coluna (ou linha) são vetores *ortonormais* com relação à $\alpha$.
- No caso das colunas, isso acontece pois, escrevendo uma matriz genérica $A$, e fazendo o produto $A^{T}A$, os elementos da diagonal $AA^{T}_{ii}$ serão o produto do vetor coluna $i$ de $A$, transposto, com ele mesmo, e pela definição de ortonormalidade, e como independente do p.i, o p.i se comporta como produto escalar, teremos o elemento $A^{T}A_{ii}= 1$, e para elementos fora da diagonal, o produto interno será $0$, pois eles serão ortogonais, o que resulta na identidade. O caso das linhas é análogo, fazendo $AA^{T}$ é possível provar.

Se $\alpha$ e $\beta$ são duas bases ortonormais de um espaço qualquer de $V$, então a matriz de mudança de base $[I]^{\alpha}_{\beta}$ é ortogonal, o que implica que $([I]^{\alpha}_{\beta})^{T}=$

O determinante ser $\pm 1$ implica que, com o determinante podendo ser $1$, a transformação descrita pela matriz não muda a orientação dos vetores no espaço, mas pode envolver rotações ou translações (mas aí não seria linear), por exemplo, rotações tem determinante $1$.

Determinante $-1$ implica que a transformação descrita pela matriz inverte a orientação do espaço, reflexões sobre eixos são exemplos desse tipo de transformação.

O determinante unitário implica que o espaço não é nem esticado nem encolhido pela transformação, ou seja, matrizes ortogonais preservam o tamanho das coisas. Veremos isso mais à frente.

____
Seja V um espaço vetorial com p.i, $\alpha$ uma base ortonormal e $T:V \rightarrow V$ um operador linear.
- $T$ é chamado de operador auto-adjunto se $[T]^{\alpha}_{\alpha}$ é uma matriz simétrica.
- $T$ é chamado de operador ortogonal se $[T]^{\alpha}_{\alpha}$ é uma matriz ortogonal.

Esses operadores estão bem definidos no sentido de um operador ser autoadjunto ou ortogonal não depende da base escolhida, isto é se $[T]_{\alpha}^{\alpha}$ for simétrica ou ortogonal numa base ortogonal $\alpha$, então $[T]^{\beta}_{\beta}$ também será simétrica para qualquer outra base ortonormal $\beta$, demonstração:

$$\begin{align*}
[T]^{\beta}_{\beta}&= ([I]^{\beta}_{\alpha})^{-1}[T]_{\alpha}^{\alpha}[I]^{\beta}_{\alpha}\\
&= ([I]^{\beta}_{\alpha})^{T}[T]_{\alpha}^{\alpha}[I]^{\beta}_{\alpha}\\
([T]^{\beta}_{\beta})^{T}&=(([I]^{\beta}_{\alpha})^{T}[T]_{\alpha}^{\alpha}[I]^{\beta}_{\alpha}) ^{T}\\
&= ([I]_{\alpha}^{\beta})^{T}([T]_{\alpha}^{\alpha})^{T}[I]^{\beta}_{\alpha}\\
&= ([I]_{\alpha}^{\beta})^{T}([T]_{\alpha}^{\alpha})[I]^{\beta}_{\alpha}\\
&= [T]^{\beta}_{\beta}
\end{align*}$$

Propriedades de Operadores AutoAdjuntos
Seja $V$ um espaço vetorial com p.i, e $T:V \rightarrow V$ linear. então $T$ auto-adjunto implica que $\innp{Tv,w}= \innp{v, Tw}$ para todo $v,w \in V$. Isso é uma consequência natural da simetria de $T$.
Pensando $Tv$ e $Tw$ não como um vetor individual, mas como a multiplicação de duas matrizes, e usando a definição matricial de produto interno, temos:
$$\begin{align*}
\innp{a,b}&= a^{T}b\\
\innp{Tv, w}&= (Tv)^{T}w\\
&= v^{T}T^{T}w\\
&= v^{T}Tw\\
&= \innp{v, Tw}
\end{align*}$$
Operadores Ortogonais estão associados a movimentos _rígidos_. Por exemplo, nos restrigindo ao $\R^{2}$, rotações de um ângulo qualquer ou reflexões sobre retas pela origem ou alguma composição dessas duas. 