---
tags: algorithms
aliases: asymptotic, big-oh, big-theta, big-omega, little-oh, little-omega
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

# Proper abuses of asymptotic notation

The first abuse of notation that we'll cover happens when the free variable tending to $\infty$ must be derived from context. When we write $O(f(n))$ we're interested in the growth of $g(n)$ as $n$ grow towards infinity. The most common situation requiring contextual knowledge of which variable tends to $\infty$ occurs when the function inside the asymptotic notation is constant, as in the expression $O(1)$. The notation solely doesn't tell us which variable is tending to $\infty$, the context must disambiguate, thus we write $f(n) = O(1)$. It's apparent which variable is growing, by the definition of $O$ notation we say that $f(n)$ is upper-bounded by some constant $c$ for values of $n$ greater than or equal to another constant $n_{0}$.
Another notational abuse that requires clarification occurs when the function is bounded by a constant, whom we use often when stating recurrences. What is conventionally meant when we write $T(n) = O(1)$ for $n \lt 3$ is that there exists a positive constant $c$ such that $T(n) \le c$ for $n \lt 3$,
this has nothing to do with the formal definition of the asymptotic notation, (*the $n_{0}$'s and shit). 

## "Little-oh" $o$-notation

The asymptotic upper bound provided by the $O$ notation may or may not be **asymptotically tight**, for example, $2n² =O(n^{2})$ is asymptotically tight, but $2n = O(n^{2})$ isn't. $o$-notation describes an upper bound that **is not** asymptotically tight, we define it as the set:
$$\begin{align*}
o(g(n))=\{f(n)\mid \forall c\gt0\exists n_{0}\gt0 \forall n &\ge n_{0} 0 \le f(n) \lt cg(n)\}
\end{align*}$$
*For any constant $c \gt 0$, exists some $n_{0}\gt 0$* such that for all $n \ge n_{0}$ the predicate is true. Notice that for $f(n)=O(g(n))$the bound $0 \le f(n) \le cg(n)$ holds for some constant $c \gt 0$, but in $f(n)=o(g(n))$ the bound $0 \le f(n)\lt cg(n)$ holds **for all** constants $c \gt 0$.   

## "Little-omega" $\omega$-notation 

By analogy, $\omega$-notation is to $\Omega$-notation what $o$-notation is to $O$-notation. We use $\omega$-notation to denote a lower bound that is not asymptotically tight. One to define it is by:
$f(n)= \omega(g(n)) \iff g(n)=o(f(n))$.

> If $f(n)$ represents a asymptotically non-tight upper bound to g(n), we kind of "flip" the graph and now $g(n)$ represents a asymptotically non-tight **lower** bound to $f(n)$.

Formally we define it as:

$$\begin{align*}
\omega(g(n))=\{f(n)\mid \forall c\gt0\exists n_{0}\gt0 \forall n &\ge n_{0} 0 \le cg(n) \lt f(n)\}
\end{align*}$$
Where the definition of $o$-notation says $f(n) \lt cg(n)$, the definition of $\omega$ says the opposite: $cg(n) \lt f(n)$. The relation $f(n) =\omega(g(n))$ implies that $f(n)$ becomes arbitrarily large compared to $g(n)$ as $n$ grows to $\infty$.