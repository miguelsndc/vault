---
tags: graphics
aliases: pipeline
---
The *graphics rendering pipeline*, or simply **the pipeline** is the multistage process that renders complex scenes to the screen, notice that each stage of the pipeline can be a pipeline in itself, and pipelines, as well as pipeline stages can be parallelized for speed. 
If a car assembly pipeline consists of several stages where each takes $2$ minutes to execute, and for example, placing the wheel takes $3$ minutes, since all of these processes run in parallel, all other tasks would be stale waiting for the wheel task to finish, the wheel task is called the **bottleneck**, the *slowest stage of a pipeline is what defines it's speed*. Speed in context of graphics can be calculated using **FPS** *(Frames Per Second)* or **Hertz**, which is simply $\frac{1}{seconds}$, the frequency of update. Hardware speed in displays is measured in hertz, $50Hz$  is the maximum frequency some display out there can put.

If we could locate the bottleneck, and measure how much time data takes to pass through that stage, we could measure the rendering speed of the pipeline to run at $20ms$, we can calculate how much 

The **Graphics** pipeline consists of three conceptual stages:
- Application stage
- Geometry stage
- Rasterization stage

