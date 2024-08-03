---
tags: graphics
aliases: model, view
---
> A model is a object on the scene, might be a sphere, a plane, a house, a person, or whatever you want to be rendered.

On it's way to the screen, a model is transformed between multiple [[Vector Space|spaces]], or *coordinate systems*, each model resides in it's own **model space** which simply means that it has not been transformed at all. Each model is associated with a model transform so it can be positioned and oriented, it is possible for a model to have multiple transforms associated to it, which allows different instances (copies) of the same model to have different orientations and positions without replicating the base geometry.
It is the vertices and the normals of the model that are transformed by the model transforms, the coordinates of an object are called **model coordinates** and once the model transform has been applied, a object is said to be on **world space**, the world coordinates are unique and after all models has been transformed by their respective model transforms, all lie on the same space.
___
Only the models that the camera sees are rendered. The camera has a location in world space and a direction, which are used to place and aim the camera. To facilitate [[Projection]] and [[Clipping]], the world space is transformed by the **View Transform**, whose purpose is to place the camera at the origin, facing the direction of the negative (or positive) $z$-axis, the $y$-axis facing up and the $x$-axis facing right.