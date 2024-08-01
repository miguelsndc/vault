---
tags: algorithms
---

*1.1-1 Describe your own real-world example that requires sorting. Describe one that requires finding the shortest distance between two points.*

Sorting - Imagine you have a scene full of objects, spheres, cylinders, cones, and so on. You cast a ray from a light source to the environment and compute the intersection points as well as which object was intersected. How do you know where the shadows should be ? where the specular light is ? By sorting the intersection points. If we assume the objects and the light source to be aligned in a line, and the ray cast is straight to the plane, then the intersection with the smallest t-value (assuming the ray is pointing at a position where the value of the axis is increasing) will have the specular light, and we render no light where the first object covers the second and so on.

Shortest-Path -  The maze problem is a classic, you have a grid where each cell might be a path, a wall, a monster, or a exit/entrance, you are lost and have only a map, with the locations of the monsters and the entrances/exits, you surprinsigly find your location there, because you have a really good memory. So know you have to calculate the shortest path to the nearest exit such that no monster can get there faster than you, you run a shortest path algorithm for you and for the monsters and hope that it outputs that you can get there faster.

*1.1-2 Other than speed, what other measures of efficiency might you need to consider in a real-world setting?*

Depending on your scenario, you might want to consider the individual characteristics of your input, the memory the 

