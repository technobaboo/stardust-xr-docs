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
### `Vector2`
A `TypedArray` of 2 `double` is treated as a `Vector2`.
### `Vector3`
A `TypedArray` of 3 `double` is treated as a `Vector3`.
### `Quaternion`
A `TypedArray` of 4 `double` is treated as a `Quaternion`.
### `Transform`
A `TypedArray` of 3 `TypedArray` containing 3 `double` is treated as a 3D transform matrix.