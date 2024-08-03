---
tags: graphics
aliases: geometry
---
The geometry stage is responsible for the majority of per-polygon and per-vertex operations. This stage is further divided into the following [[Differences between Functional, Conceptual and Pipeline Stages|functional]] stages:
- [[Model and View Transform]]
- [[Vertex Shading]]
- [[Projection]]
- [[Clipping]]
- [[Screen Mapping]]
Note that depending on the implementation, these functional stages may or may not be implemented as [[Differences between Functional, Conceptual and Pipeline Stages|pipeline]] stages, in some cases, a number of consecutive functional stages form a single pipelina stage (which runs in parallel with the other pipeline stages), in other cases, a functional stage may be subdivided into several smaller pipeline stages.