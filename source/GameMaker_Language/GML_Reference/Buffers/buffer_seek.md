# buffer_seek

This function can be used to move through a buffer, finding the start,
the end, or a position relative to that which was last used when reading
or writing data. The "offset" value is the offset (in bytes) to add to
the given seek position, for example, if the base is relative and the
offset is 4, then the buffer position will move along 4 bytes from its
current position. Please note the following:

-   You can use negative values for the offset to seek back through the
    buffer as well as positive values.
-   If the buffer is of the "wrap" type and you offset past the end of
    the buffer, the seek position will also wrap.
-   If the buffer is not of the "wrap" type, the seek will clamp to the
    beginning or end of the buffer, even when the offset would take the
    seek outside of the buffer limits.

The following constants are accepted as the "base" argument for seeking
to:

|                                                                                                |                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
|  [Buffer Seek Constant](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_seek)  |                                                        |
| Constant                                                                                       | Description                                            |
|  buffer_seek_start                                                                             | The start of the buffer                                |
|  buffer_seek_relative                                                                          | A position relative to the current read/write position |
|  buffer_seek_end                                                                               | The end of the buffer                                  |

#### Syntax:

``` gml
buffer_seek(buffer, base, offset);
```

|          |                                                                                       |                                 |
|----------|---------------------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                                  | Description                     |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to use. |
| base     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The base position to seek.      |
| offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The data offset value.          |

#### Returns:

``` gml
N/A
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
