# Model
A graphical model.

## Properties
### `setOrigin(Vector3 origin)`
Sets the origin to `origin`. 

### `setOrientation(Quat orientation)`
Sets the orientation to `orientation`. 

### `setPose(Vector3 origin, Quat orientation)`
Sets the pose using `origin` and `orientation` absolutely.

### `destroy()`
Destroys the model instance. Resources like the mesh and material and textures may be in memory still, but the resource manager will clean it up if needed.