Key-value mapping for quick read-write operations, access done key-wise.

Para encontrar em que posição deve-se colocar o valor associado a uma chave utiliza-se uma função de **hash** cujo objetivo é transformar a chave num valor único que possa ser guardado na estrutura por trás da hash table e acessado em $O(1)$ amortizado.

Possíveis estruturas para implementação de uma hash-table:
- Arrays
- Linked-Lists
- Balanced Trees
Com arrays a função de hash precisa distribuir as chaves sobre os índices do array.
Soluções triviais:
- Inteiros:
Com #number-theory  flashbacks, o módulo de um inteiro $n$ por outro inteiro $m$ **sempre será** um número entre $0$ e $m - 1$, **nem sempre isso é verdade, dada as implementações em certas linguagens**. mas a nível de exemplo, suponha que seja, então, uma possível função de hash utiliza o módulo como forma de colocar os valores numa posição acessível ao array interno.

```cpp
m = SOME_CONSTANT_VALUE;

int hash(int n) {
	return n % m;
}
```

Ou para strings, é possível utilizar a soma dos valores ascii de cada caracter:

```cpp
m = SOME_CONSTANT_VALUE;

int hash(string K) {
	s = K.size();
	int sum = 0;
	for (int i = 0; i < s; i++) {
		sum += (int) K[i];	
	}
	return abs(sum) % m;
} 
```

# Collisions

Colisões de chaves acontecem quando a função de hashing joga dois valores na mesma posição, colisões são comuns em hashmaps, por isso existem duas formas "padrão" de lidar:

## Open Hashing (Separate Chaining)

Nesta estratégia, cada célula do array corresponde à uma linked-list, e caso hajam colisões em uma posição j, a j-ésima linked list terá a chave inserida em si.
- Caso mantenha a lista ordenada: 
	- Melhor Busca; Pior inserção. $O(\log n)$ e $O(n)$, caso utilize o binary-search 
- Caso mantenha a lista desordenada:
	- Pior busca; melhor inserção. $O(n)$, caso não exista na lista é preciso percorrer todos os elementos, e para inserir basta inserir no final da lista.
Caso haja a colisão: Seja $K$ a chave que queremos encontrar tal que $h(K) = x$, vamos até a $x$-ésima lista ligada e procuramos pela chave $K$, e caso exista, retornamos o valor associado, seja ele $Y$, caso não, retornamos algum valor impossível tipo $-1$, então:

```
procedure get(key K)
	hash = h(K)
	llist = container[hash]
	traverse llist
		if element == K
			return Y
	return -1
```

## Dúvidas
- Onde os valores ficam guardados ?
- Como posso implementar uma função de hash que leve em conta um possível crescimento da capacidade do container (array) ?
- 
