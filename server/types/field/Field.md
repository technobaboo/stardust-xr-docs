# Field
Type that contains methods all Fields share. All fields created are under  `/field`.

## Properties
### `setOrigin(Vector3 origin)`
Sets the origin to `origin`. 

### `setOrientation(Quat orientation)`
Sets the orientation to `orientation`. 

### `setPose(Vector3 origin, Quat orientation)`
Sets the pose using `origin` and `orientation` absolutely. 

## Methods
### `double distance(Vector3 point)`
Returns the distance from `point` to the surface of the object, positive if the point is outside and negative if inside. When `point` is far enough away the object will give an approximate distance to the origin instead of the surface.

### `Vector3 normal(Vector3 point)`
Returns the normal of `point` compared to the surface of the object. Normal always points toward object.

### `Vector3 closestPoint(Vector3 point)`
Returns the closest point from `point` to the surface of the object. Use this instead of `distance` and `normal` when possible to limit IPC calls.