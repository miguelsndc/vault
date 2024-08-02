---
tags: graphics
aliases: application
---
The developer has full control of what happens in the application stage since it runs completely on the CPU, allowing the developer to entirely determine the implementation and can later modify it to improve performance, changes in performance here can also affect other stages, for example, some algorithm or some setting can decrease the number of triangles to be rendered.
At the end of the application stage, the **geometry** of the scene is later fed into [[The Geometry Stage]], these are *rendering primivites*, i.e points, lines, triangles, planes, or whatever might come up to the screen, this is the most important task of the application stage.
A consequence of the software-based implementation of this stage is that it's not **pipelined** and subdivided into other stages like [[The Rasterization Stage]] and [[The Geometry Stage]], but in order to increase performance this stage is often parallelized and run in multiple CPU cores.
One process commonly implemented in this stage is [[Collision Detection]], after a collision is detected between two objects, a response may be generated and the information is sent back to the two objects to perform some sort of action depending on the implementation. The application stage is also responsible for handling input from external devices, such as mouse, keyboard, lightsabers and shit.