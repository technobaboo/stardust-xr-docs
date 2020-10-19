# /input

Object managing input and interaction.

## Signals
### `registerPointerInput(string name, Vector3 origin, Vector3 direction, float tilt)`
Creates a new [[Pointerinput]] at `/input/methods/[name]` with the origin, direction, and tilt specified.

### `registerInputHandler(string name, string field, string callbackPath, string callbackMethod)`
Creates a new 