# Spatial
A base type for types that exist in 3D space, always relative to another space or the engine's world space. Spatials are always relative because in AR or XXR reference spaces change constantly in response to new environments.

## Internal Properties
Sometimes it makes sense for a Spatial to not be scalable (like in [[Field]]s where scaling dramatically increases the number of steps to raymarch for pointers) or not be rotatable (point lights) or such, so these are disabled for certain Spatial-derived objects, mentioned right after "Derived from [[Spatial]]".
### `translatable: bool`
If false, object's origin cannot be modified from a client.
### `rotatable: bool`
If false, object's rotation cannot be modified from a client (e.g. point lights, point sound sources).
### `scalable: bool`
If false, object's scale cannot be modified from a client (e.g. [[Field]]s, [[PointerInput]]s).

## Methods
### `setOrigin(Vector3 origin)`
Sets the origin to `origin`. 

### `setOrientation(Quat orientation)`
Sets the orientation to `orientation` if `rotatable` is not `false`.

### `setPose(Vector3 origin, Quat orientation)`
Sets the pose using `origin` and `orientation` relative to the pose's space if `translatable` and `rotatable` are true. This method saves on IPC calls compared to `setOrigin` and `setOrientation` in sequence.