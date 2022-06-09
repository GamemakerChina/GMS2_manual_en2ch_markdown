# buffer_base64_decode_ext

With this function you can decode a base64 encoded string (created using
the [ buffer_base64_encode() ](buffer_base64_encode) function) into
a buffer. Unlike the function [ buffer_base64_decode()
](buffer_base64_decode) , this will *not* create a buffer for you,
but rather you should already have created the buffer (see [
buffer_create() ](buffer_create) ), the id of which you would then
use with this function. The "offset" is the position within the buffer
to decode the given string (in bytes).

#### Syntax:

``` gml
buffer_base64_decode_ext(buffer, string, offset);
```

|          |                                                                                       |                                                    |
|----------|---------------------------------------------------------------------------------------|----------------------------------------------------|
| Argument | Type                                                                                  | Description                                        |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to decode the string into. |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                 | The base64 encoded string to decode.               |
| offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The data offset value.                             |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
buff = buffer_create(16384, buffer_grow, 2); ini_open("Save.ini");
 var str = ini_read_string("Save", "Slot1", ""); buffer_base64_decode_ext(buff, str, 0); ini_close();
```

The above code will create a buffer and store the unique id for it in
the variable "buff", then open an ini file and read a string from it
into the local variable "str". This string is then decoded into the
newly created buffer before closing the ini file again.
