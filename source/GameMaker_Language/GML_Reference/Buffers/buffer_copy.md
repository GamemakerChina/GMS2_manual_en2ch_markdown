# buffer_copy

This function can be used to copy a segment (or all) of the data stored
in one buffer to another. When using two buffers and copying from one to
the other, both buffers must have previously been created using the [
buffer_create() ](buffer_create) function (for example), and you can
specify a data offset (in bytes) for the start point of the data to be
copied from the source buffer relative to the start of the buffer, as
well as another data offset to define the position to copy the data to
in the destination buffer. **NOTE** : You cannot copy to the same
buffer.

#### Syntax:

``` gml
buffer_copy(src_buffer, src_offset, size, dest_buffer, dest_offset);
```

|             |                                                                                       |                                                     |
|-------------|---------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument    | Type                                                                                  | Description                                         |
| src_buffer  |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to copy *from* .            |
| src_offset  |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The data offset to start copying from (in bytes).   |
| size        |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The size of the data to copy (in bytes).            |
| dest_buffer |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to copy *to* .              |
| dest_offset |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The offset position to copy the data to (in bytes). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
buffer_copy(buff1, 0, 2048, buff2, 2048);
```

The above code will copy the data stored in the buffer indexed in the
variable "buff1", and then paste it into the buffer indexed in the
variable "buff2", but offset by 2048 bytes.
