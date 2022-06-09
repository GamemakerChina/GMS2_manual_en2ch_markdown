# buffer_fill

This function can be used to fill a previously created buffer with a
given data type and value. The data you fill the buffer with must be in
agreement with the "type" argument of this function, meaning that you
can't try to fill with a string and use the unsigned 16bit integer type,
for example. The type constants are the same as those used by the [
buffer_read() ](buffer_read) and [ buffer_write()
](buffer_write) functions. The "size" is the size of the buffer (in
bytes) that you wish to fill, while the offset is the offset value (also
in bytes) from the start of the buffer to start the fill from.

#### Syntax:

``` gml
buffer_fill(buffer, offset, type, value, size);
```

|          |                                                                                       |                                                                                                             |
|----------|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                  | Description                                                                                                 |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to fill.                                                                            |
| offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The data offset value (in bytes).                                                                           |
| type     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The type of data that is to be written to the buffer (see the list of constants [here](buffer_write) ). |
| value    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The data to write.                                                                                          |
| size     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The size of the buffer (in bytes) that you wish to fill.                                                    |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
map_buffer = buffer_create(16384, buffer_fixed, 0); buffer_fill(map_buffer, 0, buffer_u16, 0, 16384);
```

The above code finds the start of the buffer with the id stored in the
variable "buff" them writes a series of signed 16bit integer values to
it.
