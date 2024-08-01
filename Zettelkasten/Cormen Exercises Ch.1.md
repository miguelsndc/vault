---
tags: algorithms
---

*1.1-1 Describe your own real-world example that requires sorting. Describe one that requires finding the shortest distance between two points.*

Sorting - Imagine you have a scene full of objects, spheres, cylinders, cones, and so on. You cast a ray from a light source to the environment and compute the intersection points as well as which object was intersected. How do you know where the shadows should be ? where the specular light is ? By sorting the intersection points. If we assume the objects and the light source to be aligned in a line, and the ray cast is straight to the plane, then the intersection with the smallest t-value (assuming the ray is pointing at a position where the value of the axis is increasing) will have the specular light, and we render no light where the first object covers the second and so on.

Shortest-Path -  The maze problem is a classic, you have a grid where each cell might be a path, a wall, a monster, or a exit/entrance, you are lost and have only a map, with the locations of the monsters and the entrances/exits, you surprinsigly find your location there, because you have a really good memory. So know you have to calculate the shortest path to the nearest exit such that no monster can get there faster than you, you run a shortest path algorithm for you and for the monsters and hope that it outputs that you can get there faster.

*1.1-2 Other than speed, what other measures of efficiency might you need to consider in a real-world setting?*

Depending on your scenario, you might want to consider the individual characteristics of your input, the memory spent, the time obviously, which worst/average/best case efficiency trade-up is most suitable for your problem, if you need a online of offline algorithm, whether you can tradeoff space and time, your hardware (cache and stuff like that), and so on and so forth.

*1.1-3 Select a data structure that you have seen, and discuss its strengths and limitations.*

The Binary Search tree gives a good balance between lookups and insertions, striking a good average case of logarithmic time in a ideal scenario, being a more stable alternative to the hash tables, where the lookup time is amortized constant time depending on the hash function, but the collisions might take that time up to linear time in a poorly designed hash table, however binary trees are much more versatile, allowing a much wider range of use cases, such as collision systems in quake III for example. However it has a pretty wild limitation, balanced trees have height logarithmically proportional to the input, but depending on the input, or even depending on the order of the input, the tree might strike a height of $n$, and be as bad as a linked list, there are alternatives that try to minimize this problem, but introduce overheads, like rotations and coloring.

*1.1-4 How are the shortest-path and traveling-salesperson problems given above similar? How are they different?*

The traveling-salesperson is similar to the shortest path problem in the sense that the ideal solution to the traveling-salesperson is a shortest path in a weighted graph, however, it's not only a path, it's a hamiltonian cycle, where each vertex is visited exactly once. This introduces a wild change in perspective, we can try a heuristic like a minimum spanning tree, but it might not suffice, all of these minimum-weight stuff in graph derive from the idea of having a path with minimum weight, which is in fact what the shortest path problem describes.

*1.1-5 Suggest a real-world problem in which only the best solution will do. Then come up with one in which "approximately" the best solution will do.*

Everytime we deal with uncertainty and probabilities, algorithms that strike a good balance between speed/space and can output a plausible solution most likely will do, such a example is the clustering problem, where we have a shit ton of strategies that try to minimize the error function, however the most used is the "k-means" algorithm that has a simple iterative solution and does not fuck up your computer, also in situations where the entire search space needs to be considered and we have fucking $2^{n}$ possibilites, we can try heuristics to push that down, in the knapsack problem for example.

However deterministic algorithms are a must in string matching, sorting, hashing/dehashing, etc, imagine someone getting your password right just because the password system is only "good enough" ? that's wild.

*1.1-6 Describe a real-world problem in which sometimes the entire input is available before you need to solve the problem, but other times the input is not entirely available in advance and arrives over time.*

Well let's say you have to read a file and do some statistical analysis there, usually this data is collected within some time period with a handful of people, all the data is there, and will not change.

Realtime applications have to deal with incoming data, for example, let's say im a process manager in my computer, if i have a list of processes where each has a certain priority, i will run the processes with biggest priority first, and as the user messes around in the computer, priorities might change depending on where he's looking at, where he is typing, which window is being focused and so on, i need to account for that.

*1.2-1 Give an example of an application that requires algorithmic content at the application level, and discuss the function of the algorithms involved.*

Ever played agar.io ? that fun little shitty game where you are a ball and you eat other people's balls ? yeah, it has a ranking containing the player's with the biggest balls, and that list is being sorted in real time, using whether a heap, or sorting the entire list of players every frame, which is pretty wild to be honest, or whether they are using a binary tree, something is going on there, new players arrive, players eat each other, that requires some thought about how to do it, if you only allow $100$ players or so on each game, we can sort the list every frame and be cool with it, but if you allow $1000000$ players, shit gets real, (i don't even know if the browser or the server can handle that much simultaneous connections, but for curiosity sake, assuming that number) you might need a much better system to handle the ranking, you might want to benefit the structure of the data to do that, or something else, maybe realize that only small changes happen within the data structure, a player never really goes from $0$ points to $100000$ points outta nowhere, you only need tiny swaps between nodes, and account for deletions when a player dies, you can run something like a insertion sort every frame, since it runs best on somewhat sorted lists, a linked-list might not be the best case, because accounting for the overhead of pointers and the lack of locality of reference might not worth it, and c'mon, a player with a bazillion points rarely gets killed, you almost never have to move everything up one position.


*1.2-2 Suppose that for inputs of size $n$ on a particular computer, insertion sort runs in $8n^{2}$ steps and merge sort runs in $64 n \log n$ steps. For which values of $n$ does insertion sort beat merge sort?*

Let $i(n)$ and $m(n)$ be the respective functions for insertion sort and merge sort, since both and monotonically increasing (you never sort a list of $100$ elements faster than a list of $1000$ elements), we can find a intersection point and from the point above the merge sort is faster, so: 
$$\begin{align*}
8n^{2}&= 64n\log n\\
n^{2}&= 8n\log n\\
n &= 8\log n\\
\frac{n}{8}&= \log n\\
2^{\frac{n}{8}=}n
\end{align*}$$