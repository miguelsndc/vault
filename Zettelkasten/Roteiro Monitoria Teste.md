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