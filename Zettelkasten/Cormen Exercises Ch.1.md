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

The traveling-salesperson is similar to the shortest path problem in the sense that the ideal solution to the traveling-salesperson is a shortest path in a weighted grea