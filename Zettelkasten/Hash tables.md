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

Nesta estratégia