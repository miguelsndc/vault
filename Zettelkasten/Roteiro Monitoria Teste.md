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