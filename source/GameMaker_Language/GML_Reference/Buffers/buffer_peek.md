# buffer_peek

With the [ buffer_read() ](buffer_read) function, you can read data
from the given buffer at the current "seek" position, with each piece of
data being read advancing this position by the bytes being read or
written. However, it may be necessary for you to read a given piece of
data without wanting to change the current seek position, and that's
when you would use this function. You simply supply the function with a
buffer id, and then an offset position (from the buffer start) within
that buffer to read from, as well as the data type that you are wanting
to read. **NOTE** : Using the incorrect data type for the data being
read will result in erroneous values! If the function succeeds then a
value (Real, string, boolean, etc...) will be returned depending on the
data type, while a failure will return simply 0.

#### Syntax:

``` gml
buffer_peek(buffer, offset, type);
```

|          |                                                                                                      |                                                                                                           |
|----------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                 | Description                                                                                               |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                 | The index of the buffer to use.                                                                           |
| offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                  | The offset position (in bytes) within the buffer to read the given data from.                             |
| type     |  [Buffer Data Type Constant](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_write)  | The type of data that is to be read from the buffer (see the list of constants [here](buffer_read) ). |

#### Returns:

``` gml
 Real

,

 Boolean

,

 String

or 0 (if it fails)
```

#### Example:

``` gml
var red = buffer_peek(buff, 1, buffer_u8);
var green = buffer_peek(buff, 2, buffer_u8);
var blue = buffer_peek(buff, 3, buffer_u8);
image_blend = make_colour_rgb(red, green, blue);
```

The above code will get three values from three different positions
within the buffer indexed in the variable "buff" and then use those
values to set the image blend of the instance.
