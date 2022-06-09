# buffer_crc32

This function will take input data from a buffer and returns a crc32
checksum hash. You specify the buffer ID of the buffer to use, then an
offset value (in bytes) for where to begin, and then a size (again in
bytes) for the region to be hashed, and the function will return a 32
bit integer value for that region.

#### Syntax:

``` gml
buffer_crc32(buffer, offset, size);
```

|          |                                                                                       |                                 |
|----------|---------------------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                                  | Description                     |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to use. |
| offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The data offset value.          |
| size     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The size of the buffer.         |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
check_val = buffer_crc32(buff, 0, buffer_get_size(buff));
```

The above code will create a crc32 checksum hash value for the full data
stored in the buffer indexed by the variable "buff", and store the
returned integer hash value in the variable "check_val".
