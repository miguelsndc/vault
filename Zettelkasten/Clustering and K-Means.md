Clustering se refere ao leque de estratégias para encontrar *subgrupos* ou *clusters* dentro de um conjunto de dados. 
Procura-se particionar os dados em subconjuntos disjuntos tais que as observações *( ou amostras)* dentro de cada subconjunto são similares, e observações em clusters diferentes diferem razoavelmente.
Claro que para isso se concretizar, se faz necessário definir o que significa ser "similar" e "diferente", isso é uma decisão específica do domínio sendo trabalhado, e deve ser feita a partir do conhecimento dos dados estudados.

Suponha que temos um conjunto de $n$ amostras, cada uma com $p$ variáveis. *A nível de exemplo*, as $n$ observações poderiam corresponder à $n$ amostras de tecido dos tumores de pacientes com câncer de mama, e cada uma das $p$ variáveis, algum tipo de medição clínica, como grau ou estágio do tumor.
Poderíamos ter um motivo pra acreditar que existe alguma heterogeneidade entre as $n$  amostras, e talvez haja um subtipo *desconhecido* de câncer de mama. Técnicas de clustering podem ser usadas para encontrar esses subtipos.

- Clustering é um problema **não-supervisionado**, porque estamos tentando descobrir alguma *estrutura* nos dados, nesse caso, clusters distintos, nas bases de um conjunto de dados.

Outra aplicação para clusterização aparece em *marketing*. Suponha que temos acesso a um grande número de medições feitas em um grande número de pessoas, como renda média, distância da área urbana mais próxima, ocupação, e zas e zas. Nosso objetivo é executar uma *segmentação de mercado*, isto é, dividir essas pessoas em subgrupos onde cada subgrupo seja mais receptivo a um tipo específico de propagandas, ou tenha maior probabilidade de comprar algum produto, clusterização pode ser utilizada para este fim.

Como clustering é uma técnica muito popular em várias áreas, existem vários métodos de clusterização, em $k$-means, o número de clusters é pré-determinado, um número $k$ é passado como parâmetro e o algoritmo tentará, dividir os dados em $k$ clusters distintos.

Enfim, para expressar melhor as ideias, vou usar uma notação matemática. Sejam $C_{1}, C_{2}, \cdots, C_{k}$, os $k$ clusters que o algoritmo vai pegar os dados e distribuir entre. Esses conjuntos satisfazem as propriedades:
$$\begin{align*}
\begin{cases}
C_{1}\cup C_{2} \cup\cdots\cup C_{k}&= \{1, \cdots,n\}\\
C_{i}\cap C_{j}&= \emptyset \text { para } i \ne j
\end{cases}
\end{align*}$$
Como foi dito anteriormente, os clusters são subconjuntos disjuntos do espaço amostral. A nível de exemplo, se a $i$-ésima amostra está no $k$-ésimo cluster, então $i \in C_{k}$. A ideia por trás do $k$-means é que uma ***boa*** clusterização é uma feita de tal forma que a variação dentro do cluster é a menor possível, de acordo com o método utilizado para distinguir as amostras.

A variação dentro do cluster para um cluster $C_{k}$ é uma medida $W(C_{k})$ da quantidade pela qual as observações dentro de um cluster diferem umas das outras, então o problema a se resolver é:
$$
\min\limits_{C_{1}, \cdots, C_{k}} \bigg\{\sum\limits_{k=1}^{K} W(C_{k}\bigg\} 
$$
O que essa fórmula diz é que queremos particionar as amostras em $K$ clusters de tal forma que a soma de todas as $K$ variações dentro dos clusters seja a menor possível.
Resolver esse treco aí parece uma ideia razoável, mas antes, é preciso definir como será calculada essa variação dos clusters, Existem muitas formas de fazer isso, mas de longe a escolha mais comum é a pura e simples **distância euclidiana**.

Então, se temos $n$ amostras e $p$ variáveis, seguindo a lógica, como a distância euclidiana é uma operação que recebe apenas dois vetores como parâmetro, precisamos calcular a distância entre **todos os pares de vetores para cada variável $i \in p$**, e depois encontrar a média dividindo o resultado pelo número de amostras, pra facilitar a vida vamos usar a distância ao quadrado, então fica mais ou menos assim:

$$\begin{align*}
W(C_{k}) &= \frac{1}{|C_{k}|} \sum\limits_{i,i' \in C_{k}}\sum\limits_{j=1}^{p}(x_{ij}-x_{i'j})^{2}
\end{align*}$$
- $\frac{1}{|C_{k}|}$ é o inverso da quantidade de amostras dentro do cluster $k$.
- $\sum\limits_{i,i'\in C_{k}}$ estamos iterando sobre todos os pares de vetores dentro de $C_{k}$ 
 - $\sum\limits_{j=1}^{p} (x_{ij}-x_{i'j})^{2}$ estamos iterando sobre cada variável de $j$ de $p$, e calculando a distância, entre os vetores $x_{i}$ e $x_{i'}$ em relação a variável $j$.

Então, falando chique, a variação dentro dos clusters é a soma dos quadrados de todas as distâncias euclidianas entre as amostras no $k$-ésimo cluster, dividido pelo número de observações nesse cluster, então combinando tudo, ficamos com o problema de otimização (c1 flashbacks):

$$\begin{align*}
\min\limits_{C_{1}, \cdots, C_{k}} \bigg\{\sum\limits_{k=1}^{K} \frac{1}{|C_{k}|} \sum\limits_{i,i' \in C_{k}}\sum\limits_{j=1}^{p}(x_{ij}-x_{i'j})^{2} \bigg\} 
\end{align*}$$
esse treco aí é o k-means. agora a bronca é encontrar um algoritmo que resolva esse problema, isto é, um método para particionar as amostras em $K$ clusters tal que a variação dentro dos clusters é minimizada.

--- TODO: Escrever e explicar o algoritmo do k-means ---