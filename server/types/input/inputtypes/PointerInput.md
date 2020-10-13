# PointerInput
### Derived from [[InputMethod]]

An input method for pointers, 

## Methods
### `setDirection(Vector3 direction)`
Sets the direction the pointer is pointing in stage space.
### `setTilt(float angle)`
Sets the tilt of the pointer (rotation about the pointer direction) clockwise in radians.
### `setOrientation(Vector3 direction, float angle)`
Sets the direction and tilt of the pointer to save on IPC calls.
### `setPose(Vector3 origin, Vector3 direction, float angle)`
Sets the origin, direction, and tilt of the pointer to save on IPC calls.