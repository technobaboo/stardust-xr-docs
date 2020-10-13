# HandInput
### Derived from [[InputMethod]]

A full 27-bone hand+forearm input with useful abstractions provided through the datamap.

The local space of a hand is where +Z is away from the palm, +Y is from the palm to the fingers, and +X is orthogonal and to the right.

## Internal Properties
### `pose`
A multidimensional array describing a whole hand pose of the format

```html
[
	
	[Wrist position (Vector3)],
	[
		[Arm (wrist->elbow) orientation (Quaternion)],
		[Arm thickness (float)]
		[Elbow position (Vector3)]
	]
]
```
(This section is WIP)

## Datamap
### Required
| Key             | Value Type                  | Description                                                        |
|-----------------|-----------------------------|--------------------------------------------------------------------|
| confidence      | `float` (range `0.0`-`1.0`) | How confident the hand tracker is of the pose of the hand          |
| isLeft   | `bool` | `true` if this hand is the left hand, `false` if not |
| pinchStrength   | `float` (range `0.0`-`1.0`) | How much the hand is pinching                                      |
| pinchDistance   | `float` (>`0.0`)            | The distance in meters between the thumb and index finger |
| grabStrength    | `float` (range `0.0`-`1.0`) | How much the hand is making a fist                                 |
| fingerDirection | `Vector3` (direction)       | The average direction all fingers are pointing towards             |


## Methods
**TODO**: Properly secured field distance calculation accessible to clients