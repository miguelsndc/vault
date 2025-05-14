---
tags: maratona
---

### Missing coin sum - 2183

Qual a menor soma que **não** pode ser criada usando um subconjunto dos numeros dados ? Seja $s$ a soma de todos os valores de um prefixo ordenado do array + 1, então é possível criar as somas no intervalo $[1,s -1]$, assuma que o próximo elemento é estritamente maior que $s$. então as somas que não incluem esse elemento caem no interval $[1, s]$ e as somas incluindo esse elemento serão estritamente maiores que $s$. então as somas possíveis caem nos intervalos $[1,s-1]$ e $[s + 1, \cdots]$. logo $s$ é a menor soma possível.