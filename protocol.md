# Protocol
## Data
Every message uses flatbuffers and most use flexbuffers to add variant data such as method arguments and return values. The flatbuffers Message type is:

```c
namespace StardustXR;

table Message {
	type: ubyte;
	id: uint;
	object: string;
	method: string;
	error: string;
	data:[ubyte] (flexbuffer);
}

root_type Message;
```

## Message Types
### 0: Error

## Data Types
### Vector2
A `TypedVector` of 2 `double` is treated as a `Vector2`.
### Vector3
A `TypedVector` of 3 `double` is treated as a `Vector3`.
### Quaternion
A `TypedVector` of 4 `double` is treated as a `Quaternion`.
### Pose
A `Vector` containing a `Vector3` and a `Quaternion` is treated as a `Pose`.
### Transform
A `TypedVector` of 3 `TypedVector` containing 3 `double` is treated as a 3D transform matrix.