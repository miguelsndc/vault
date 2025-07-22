---
tags: cp
---

## Techniques

##### Event Sorting

Existe alguma coisa que a gente quer saber sobre um determinado intervalo, e certos eventos acontecem, algo entra em $x$ e sai em $y$,  parece um sweep line, podemos descobrir as respostas. Limitando as respostas aos subintervalos que importam, tipo, a resposta é só o que está em $[a,b]$. desconsideramos tudo que começa depois de $b$ e termina antes de $a$, e tudo que começa antes de $a$ a gente empurra pra $a$, pra poder processar de uma vez quando chegar em $a$, e tudo que termina depois de $b$ a gente joga pra $b$.

Distinguindo os eventos por "termina" ou "começa", se a gente ordenar pelo tempo podemos manter variáveis ou estruturas que nos dizem o estado atual da coisa. A ideia central gira em torno de ter uma variavel $last\_time$ que nos diz qual o tempo que passou desde o ultimo evento, fazendo $T - last\_time$ temos quanto tempo passou, e podemos fazer coisas com isso (geralmente).

um código que faz algo parecido é:

```cpp

#include <bits/stdc++.h>
using namespace std;
typedef long long ll;

int main() {
	ios::sync_with_stdio(false);
	cin.tie(nullptr);
	cout.tie(nullptr);
	ll n, s, f; cin >> n >> s >> f;
	ll st, ed;
	vector<pair<ll,ll>> v;
	for(int i=0; i<n;i++) {
		cin >> st >> ed;
		if (ed < s || st > f) continue;
		v.push_back({max(st,s), 1});
		v.push_back({min(ed,f), 0});
	}
	sort(v.begin(),v.end());
	ll lt = s, ops = 0;
	vector<ll> c(1000005);
	for (auto [T, open]: v) {
		c[ops] += T - lt;
		ops += (open == 1 ? 1: -1);
		lt = T;
	}
	if (lt < f) {
		c[ops] += f - lt;
	}
	vector<ll> a(n + 1);
	for (int i = 1; i <= n; i++) {
		a[i] = (ll)a[i - 1] + c[i - 1];
	}
	for (int i = 1; i <= n; i++) cout << a[i] << ' ';
}
```

esse simplesmente calcula a quanto tempo cada quantidade de intervalo aberto fica aberto. Um caso especial é quando **o last time não chega no $b$, no fim do intervalo**, e precisamos considerar esse cara pq nada acontece, e todos os intervalos abertos continuam abertos.