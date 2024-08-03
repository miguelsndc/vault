---
tags: graphics
aliases: functional, conceptual, pipeline, stage, stages
---
We differentiate between the *conceptual stages:* [[The Application Stage|application]], [[The Geometry Stage|geometry]] and [[The Rasterization Stage|rasterization]] stages (which are conventions), functional and pipeline stages. 
A **functional** stage has a certain task to perform but *does not specify* the way that task is executed in the pipeline. 
A **pipeline** stage, on the other hand, is executed in parallel with all the other pipeline stages. A pipeline stage may also be parallelized to meet performance needs, for instance, the [[The Geometry Stage|geometry]] stage consists of five functional stages, but it is the implementation of a graphics system that determines it's subdivision into pipeline stages. A given implementation may combine two functional stages into a pipeline stage, while divides another, most time consuming into it's own pipeline stage to  run in parallel.