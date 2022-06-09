# buffer_sizeof

This function will return the size (in bytes) of the given [Buffer Data
Type
Constant](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_write)
(listed [here](buffer_write) ).

#### Syntax:

``` gml
buffer_sizeof(type);
```

|          |                                                                                                      |                                                                                              |
|----------|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                 | Description                                                                                  |
| type     |  [Buffer Data Type Constant](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_write)  | The type of data that is to be checked (see the list of constants [here](buffer_read) ). |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var b = 12 * buffer_sizeof(buffer_u8);
buff = buffer_create(b, buffer_fixed, 1);
```

The above code first calculates the size of the buffer to create by
multiplying the unsigned 8bit data type by 12 (since we will be using
the buffer to hold 12 pieces of data), and then uses this value to set a
fixed buffer to the correct size.
