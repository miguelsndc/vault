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

$\Theta$ notation characterizes an **tight bound** on the asymptotic behavior of a function. It says that a function grows **precisely** at a certain rate, based, once again - on the highest order term -. Put another way, $\Theta$ notation characterizes a rate of growth to within a constant factor from above and to within a constant factor from below, These two constant factors need not be equal.
If you can show that a function is both in $O(f(n))$ and $\Omega(f(n))$ for some function $f$ you have shown that this function is in $\Theta(f(n))$. 

## Avoid Overstating and choose the most precise notation possible

Whenever you're describing an algorithm's running time with asymptotic notation, use a bound-function that describes the running time as precise as possible, do not **obscure** the running time with confusing and perhaps **uncanny** use of $O,\Theta$ and $\Omega$. 
Take **insertion sort** as an example, the worst-case running time of insertion sort is $O(n^{2}), \Theta(n^{2})$ and $\Omega(n^{2})$, Although the three ways to characterize the worst-case running time are correct, $\Theta(n^{2})$ is the most precise and hence the preferred way. We can also say that the **best**-case running time of insertion sort is in $O(n),\Theta(n)$ and $\Omega(n)$, $\Theta(n)$ being the most precise and thus the preferred.
**What we cannot say** is: *Insertion sort's running time is $\Theta(n^{2})$*. That's an overstatement because by omitting the "worst case" from the statement we're left with a blanket covering all cases. The error here is that insertion sort does not run in $\Theta(n^{2})$ in all cases, as we've seen, it runs in $\Theta(n)$ for it's best case. We can correctly say that insertion sort's running time is $O(n^{2})$ as we've seen because that establishes a upper-bound, it is okay to have cases where the running time grows more slowly than $n^{2}$.
Another common mistake is using the $O()$ notation to describe **asymptotically tight-bounds**, with statements such as *"An algorithm that runs in $O(n \lg n)$ runs faster than an algorithm that runs in $O(n^{2})$"*, we actually don't know, maybe it does, maybe it doesn't, since $O$ only describes an upper bound for the function we might have cases where the $O(n^{2})$ algorithm outperforms the linearithmic one.
See **Merge Sort** as an example, it runs in $O(n \lg n), \Theta(n \lg n), \Omega(n\lg n)$; here is safe to say that merge sort runs in $\Theta(n \lg n)$ without specifying worst-case or best-case.

# Asymptotic notation in equations and inequalities

 When asymptotic notation stands alone on the right side of an equation (or inequality), the equal sign means set membership: $4n^{2}+100n +52 = O(n) \implies 4n^{2}+100n +52 \in O(n)$.
 In general when a asymptotic notation appears in a formula, we interpret it as an anonymous function that we don't care to name. For example the formula: $4n^{2}  + 100n + 52 = 2n^{2} +\Theta(n)$ means that $4n^{2}+100n+52 = 2n^{2}+f(n)$ where $f(n) \in \Theta(n)$,
 Using asymptotic notation in this manner can help eliminate clutter and inessential details in an equation, allowing us to have a clearer sight of the general intention behind the formula.