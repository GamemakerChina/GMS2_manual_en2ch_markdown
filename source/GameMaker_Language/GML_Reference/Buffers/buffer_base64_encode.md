# buffer_base64_encode

This function will convert the data from the given buffer into a base64
format encoded string. This is a commonly used encoding scheme that is
often used for any media that needs to be stored or transferred over the
internet as text, and renders the output unreadable to the human eye. To
use this you need to specify an already created buffer, the offset value
(which is the point within the buffer at which you wish to start
encoding) as well as the size, in bytes, of the buffer memory to encode.

#### Syntax:

``` gml
buffer_base64_encode(buffer, offset, size);
```

|          |                                                                                       |                                 |
|----------|---------------------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                                  | Description                     |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to use. |
| offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The data offset value.          |
| size     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The size of the buffer.         |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var b_str = buffer_base64_encode(buff, 0, buffer_get_size(buff))
```

The above code will create encode the full data stored in the buffer
indexed by the variable "buff", and store the returned string in the
local variable "b_str".
