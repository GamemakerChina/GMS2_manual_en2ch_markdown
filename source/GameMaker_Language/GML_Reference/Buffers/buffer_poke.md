# buffer_poke

With the [ buffer_write() ](buffer_write) function, you can write
data to the given buffer at the current "seek" position, with each piece
of data advancing this position by the bytes being written or read.
However, it may be necessary for you to change a given piece of data
without wanting to change the current seek position, and that's when you
would use this function. You simply supply the function with a buffer
index, and then the offset position from the buffer start (in bytes)
within that buffer to write to, as well as the data type and the value
to be written.

#### Syntax:

``` gml
buffer_poke(buffer, offset, type, value);
```

|          |                                                                                                      |                                                                                                             |
|----------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                 | Description                                                                                                 |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                 | The index of the buffer to use.                                                                             |
| offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                  | The offset position (in bytes) within the buffer to write the given data to.                                |
| type     |  [Buffer Data Type Constant](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_write)  | The type of data that is to be written to the buffer (see the list of constants [here](buffer_write) ). |
| value    |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                     | The data to add to the buffer, in accordance with the type specified.                                       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
buffer_poke(buff, 3, buffer_u8, colour_get_blue(image_blend));
```

The above code will add the blue component value of the colour used for
the image blend into the buffer indexed in the variable "buff", at the
third position in the buffer and as an unsigned 8bit value.
