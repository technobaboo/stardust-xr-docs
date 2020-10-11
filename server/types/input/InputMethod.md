# InputMethod
Represents an input device generically, with specifics being fleshed out in subclasses.

## Internal properties
### `type: uint8`
|   | Name         | Description                                                                                                 |
|---|--------------|-------------------------------------------------------------------------------------------------------------|
| 0 | `Global`     | A non-spatial input, used for power buttons and system volume and such                                      |
| 1 | `Controller` | Contains a pose and datamap for buttons, trackpad, joystick, grip, trigger, etc.                            |
| 2 | `Pointer`    | Defined by origin, direction, and tilt with datamap for buttons, trackpad, etc.                             |
| 3 | `Hand`       | Contains a full 27-bone hand skeleton (+forearm) and datamap for abstractions like grip, pinch amount, etc. |

## Methods
### `setPosition(Vector3 point)`
Sets the position of this [[InputMethod]]. This pose also defines the main interaction point.

### `modifyDatamap(Dictionary data)`
Modifies the datamap of this [[InputMethod]]. Keys are of type `String` and values are of type `bool`, `float`(0-1), `Vector2`(each component being `-0.5` to `0.5`), or `Vector3` (same clamping as `Vector2`). Each key here will add to the datamap if not present and set the existing value if present. Any key not present in `data` will be unaffected.