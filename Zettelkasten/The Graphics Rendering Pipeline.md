---
tags: graphics
aliases: pipeline
---
The *graphics rendering pipeline*, or simply **the pipeline** is the multistage process that renders complex scenes to the screen, notice that each stage of the pipeline can be a pipeline in itself, and pipelines, as well as pipeline stages can be parallelized for speed. 
If a car assembly pipeline consists of several stages where each takes $2$ minutes to execute, and for example, placing the wheel takes $3$ minutes, since all of these processes run in parallel, all other tasks would be stale waiting for the wheel task to finish, the wheel task is called the **bottleneck**, the *slowest stage of a pipeline is what defines it's speed*. Speed in context of graphics can be calculated using **FPS** *(Frames Per Second)* or **Hertz**, which is simply $\frac{1}{seconds}$, the frequency of update. Hardware speed in displays is measured in hertz, $50Hz$  is the maximum frequency some display out there can put.

If we could locate the bottleneck, and measure how much time data takes to pass through that stage, we could measure the rendering speed. If we assume the bottleneck takes $20ms$ to execute, the rendering speed would then be $\frac{1}{0.020}=50hz$, however, this is not always true since it depends on the frequency of the display, and may be slower.

The **Graphics** pipeline consists of three conceptual stages:
- Application stage
[[The Application Stage]] is, as the name suggests, driven by the application and therefore is implemented in software running in general-purpose **CPU's**, these CPU's consists of multiple *cores* that are capable of running multiple *threads of execution* in parallel. This enables the CPU to run variety of tasks, the most common being *collision detection, physics simulations, global acceleration algorithms, animation* and many others.
-  Geometry stage
[[The Geometry Stage]] deals with [[Linear Transformations|transformation]]s, [[Projection onto Subspaces|projections]], etc. It decides what should be drawn, where it should be drawn and how it should be drawn, this stage runs on the GPU with several programming core as well as fixed-hardware instructions.
- Rasterization stage
[[The Rasterization Stage]] draws (renders) objects to the screen with the data provided by the previous stage, as well as performing some per-pixel computations depending on the needs, this is processed exclusively on the GPU.

