Clustering se refere ao leque de estratégias para encontrar *subgrupos* ou *clusters* dentro de um conjunto de dados. 
Procura-se particionar os dados em subconjuntos disjuntos tais que as observações *( ou amostras)* dentro de cada subconjunto são similares, e observações em clusters diferentes diferem razoavelmente.
Claro que para isso se concretizar, se faz necessário definir o que significa ser "similar" e "diferente", isso é uma decisão específica do domínio sendo trabalhado, e deve ser feita a partir do conhecimento dos dados estudados.

Suponha que temos um conjunto de $n$ amostras, cada uma com $p$ variáveis. *A nível de exemplo*, as $n$ observações poderiam corresponder à $n$ amostras de tecido dos tumores de pacientes com câncer de mama, e cada uma das $p$ variáveis, algum tipo de medição clínica, como grau ou estágio do tumor.
Poderíamos ter algum motivo pra acreditar que existe alguma heterogeneidade entre as $n$  amostras, e talvez haja algum subtipo *desconhecido* de câncer de mama. Técnicas de clustering podem ser usadas para encontrar esses subtipos.

- Clustering é um problema **não-supervisionado**, porque estamos tentando descobrir alguma *estrutura* nos dados, nesse caso, clusters distintos, nas bases de um conjunto de dados.

Outra aplicação para clusterização aparece em *marketing*, suponha que temos acesso a um grande número de medições feitas em um grande número de pessoas, como renda média, distância da área urbana mais próxima, ocupação, e zas e zas. Nosso objetivo é executar uma *segmentação de mercado*, isto é, dividir essas pessoas em subgrupos onde cada subgrupo seja mais receptivo a um tipo específico de propagandas, ou tenha maior probabilidade de comprar algum produto, clusterização pode ser utilizada para este fim.

Como clustering é uma técnica muito popular em várias áreas, existem vários métodos de clusterização, em $k$-means, o número de clusters é pré-determinado, um número $k$ é passado como parâmetro e o algoritmo tentará, dividir os dados em $k$ clusters distintos.

Enfim, para expressar melhor as ideias, vou usar uma notação matemática. Sejam $C_{1}, C_{2}, \cdots, C_{k}$, os $k$ clusters que o algoritmo vai pegar os dados e distribuir entre. Esses conjuntos satisfazem as propriedades:
$$\begin{align*}
\begin{cases}
C_{1}\cup C_{2} \cup\cdots\cup C_{k}&= \{1, \cdots,n\}\\
C_{i}\cap C_{j}&= \emptyset \text { para } i \ne j
\end{cases}
\end{align*}$$
Como foi dito anteriormente, os clusters são subconjuntos disjuntos do espaço amostral. A nível de exemplo, se a $i$-ésima amostra está no $k$-ésimo cluster, então $i \in C_{k}$. A ideia por trás do $k$-means é que uma ***boa*** clusterização é uma tal que a variação dentro do cluster é a menor possível, de acordo com o método utilizado para distinguir amostras parecidas e diferentes.

A variação dentro do cluster para um cluster $C_{k}$ é uma medida $W(C_{k})$ da quantidade pela qual as observações dentro de um cluster diferem umas das outras, então o problema a se resolver é:
$$
\min\limits_{C_{1}, \cdots, C_{k}} \bigg\{\sum\limits_{k=1}^{K} W(C_{k}\bigg\} 
$$
O que essa fórmula diz é que queremos particionar as amostras em $K$ clusters de tal forma que a soma de todas as $K$ variações dentro dos clusters, 

