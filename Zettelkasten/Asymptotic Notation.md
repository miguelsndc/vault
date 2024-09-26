---
tags: algorithms
aliases: asymptotic
---
The **asymptotic** efficiency of an algorithm tries to shed some light on the behaviour of that algorithm when the input sizes **tend to infinity**, quite literally from the concept of [[Epsilon-Delta Definition of a Limit|limits]] from calculus, usually an algorithm that is asymptotically more efficient tends to be more efficient on all but some small inputs.

Those asymptotic notations work for [[Functions]] in general, not only algorithms, they happen to be quite a fit for measuring efficiency of algorithms but **are not limited to algorithms**, in fact they're used to characterize **space** and even other types of functions, There are three types:
___
# $O$ Notation

$O$-notation characterizes an *upper bound* on the asymptotic behavior of a function. In other words, it says that a function grows *no faster* than a certain rate, based on the highest order term. Consider, as an example, the function $3n³ +4n² -100n+500$, the highest order term is $3n³$, hence it is in $O(n^{3})$ because it grows no faster than a cubic rate, in fact, it's also in $O(n^{4})$ for the same reason, and also $O(n^{5}), O(n^{6})$, and any $O(n^{c}), c \ge 3$. It is not quite useful to randomly spit large rates as it won't tell much about the function, *the smallest rate such that the function grows no faster than, should be the desired*.
## $\Omega$ Notation

$\Omega$ notation characterizes an *lower bound* on the asymptotic behavior of a function. It states that a function grows **at least as fast** as a certain rate, based - as the $O$-notation, on the highest order term- because the highest term in $3n³ +4n² -100n+500$ is $3n^{3}$, this function is in $\Omega(n^{3})$, it is also in $\Omega(n^{2}), \Omega(n)$ and so on. Just like with $O$-notation, arbitrarily small rates won't tell much about the function, it should really be the *highest rate such that the function grows at least as fast as*. 

## $\Theta$ Notation

$\Theta$ notation characterizes an **tight bound** on the asymptotic behavior of a function. It says that a function grows **precisely** at a certain rate, based, once again - on the highest order term -. Put another way   