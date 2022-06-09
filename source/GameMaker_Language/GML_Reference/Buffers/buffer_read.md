# buffer_read

This function can be used to read data from a previously created buffer.
The return value will depend on the type of data that you are reading,
which in itself is defined by the following constants:

|                 |                                                                                                                                    |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------|
| Constant        | Description                                                                                                                        |
|  buffer_u8      | An unsigned, 8bit integer. This is a positive value from 0 to 255.                                                                 |
|  buffer_s8      | A signed, 8bit integer. This can be a positive or negative value from -128 to 127 (0 is classed as positive).                      |
|  buffer_u16     | An unsigned, 16bit integer. This is a positive value from 0 - 65,535.                                                              |
|  buffer_s16     | A signed, 16bit integer. This can be a positive or negative value from -32,768 to 32,767 (0 is classed as positive).               |
|  buffer_u32     | An unsigned, 32bit integer. This is a positive value from 0 to 4,294,967,295.                                                      |
|  buffer_s32     | A signed, 32bit integer. This can be a positive or negative value from -2,147,483,648 to 2,147,483,647 (0 is classed as positive). |
|  buffer_u64     | An unsigned 64bit integer.                                                                                                         |
|  buffer_f16     | A 16bit float. This can be a positive or negative value within the range of +/- 65504. *(Not currently supported!)*                |
|  buffer_f32     | A 32bit float. This can be a positive or negative value within the range of +/-16777216.                                           |
|  buffer_f64     | A 64bit float.                                                                                                                     |
|  buffer_bool    | A boolean value. Can only be either 1 or 0 ( true or false )                                                                       |
|  buffer_string  | A string of any size.                                                                                                              |
|  buffer_text    | A string of any size, without the final null terminating character.                                                                |

If the function succeeds it will return a value of the given type,
however if it fails then it will cause a runner error. NOTE Using the
incorrect data type for the data being read will result in erroneous
values being returned.

#### Syntax:

``` gml
buffer_read(buffer, type)
```

|          |                                                                                                      |                                                                                        |
|----------|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Argument | Type                                                                                                 | Description                                                                            |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                 | The index of the buffer to read from.                                                  |
| type     |  [Buffer Data Type Constant](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_write)  | The type of data that is to be read from the buffer (see the list of constants above). |

#### Returns:

``` gml
 Real

,

 Boolean

or

 String
```

#### Example:

``` gml
var cmd = buffer_read(buff, buffer_s16);
```

The above code reads from the buffer with the id stored in the variable
"buff" a signed 16bit value into the local variable "cmd".
