# buffer_write

This function can be used to write data to a previously created buffer.
The data you write must be in agreement with the "type" argument of this
function, meaning that you can't try to write a string as an unsigned
16bit integer, for example. The following constants can be used to
define the data type:

|                                                                                                      |                                                                                                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
|  [Buffer Data Type Constant](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_write)  |                                                                                                                                    |
| Constant                                                                                             | Description                                                                                                                        |
|  buffer_u8                                                                                           | An unsigned, 8bit integer. This is a positive value from 0 to 255.                                                                 |
|  buffer_s8                                                                                           | A signed, 8bit integer. This can be a positive or negative value from -128 to 127 (0 is classed as positive).                      |
|  buffer_u16                                                                                          | An unsigned, 16bit integer. This is a positive value from 0 - 65,535.                                                              |
|  buffer_s16                                                                                          | A signed, 16bit integer. This can be a positive or negative value from -32,768 to 32,767 (0 is classed as positive).               |
|  buffer_u32                                                                                          | An unsigned, 32bit integer. This is a positive value from 0 to 4,294,967,295.                                                      |
|  buffer_s32                                                                                          | A signed, 32bit integer. This can be a positive or negative value from -2,147,483,648 to 2,147,483,647 (0 is classed as positive). |
|  buffer_u64                                                                                          | An unsigned 64bit integer.                                                                                                         |
|  buffer_f16                                                                                          | A 16bit float. This can be a positive or negative value within the same range as a 16 bit signed integer.                          |
|  buffer_f32                                                                                          | A 32bit float. This can be a positive or negative value within the same range as a 32 bit signed integer.                          |
|  buffer_f64                                                                                          | A 64bit float.                                                                                                                     |
|  buffer_bool                                                                                         | A boolean value. Can only be either 1 or 0 ( true or false )                                                                       |
|  buffer_string                                                                                       | A string of any size, finalized with a null terminating character.                                                                 |
|  buffer_text                                                                                         | A string of any size, without the final null terminating character.                                                                |

The function will return 0 if it succeeds or -1 if it fails.

#### Syntax:

``` gml
buffer_write(buffer, type, value)
```

|          |                                                                                       |                                                                                         |
|----------|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| Argument | Type                                                                                  | Description                                                                             |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to write to.                                                    |
| type     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The type of data that is to be written to the buffer (see the list of constants above). |
| value    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The data to write.                                                                      |

#### Returns:

``` gml
 Real

(0 if success, or -1 if it fails)
```

#### Example:

``` gml
buffer_seek(buff, buffer_seek_start, 0);
buffer_write(buff, buffer_s16, 0);
buffer_write(buff, buffer_s16, x);
buffer_write(buff, buffer_s16, y);
```

The above code finds the start of the buffer with the id stored in the
variable "buff" them writes a series of signed 16bit integer values to
it.
