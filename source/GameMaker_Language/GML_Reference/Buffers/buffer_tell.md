# buffer_tell

When you read or write data to a buffer using the [ buffer_read()
](buffer_read) or [ buffer_write() ](buffer_write) the current
"seek" position is advanced by the bytes written or read, and with this
function you can get the current "seek" position for use in other buffer
functions. For example, if your buffer alignment is set to 4 bytes and
you write a single piece of data which is 1 byte in size then do a
buffer_tell() , you'll get an return value of 1. However, if you write
another piece of data, also 1 byte in size, then do a buffer_tell() ,
you'll get a return value of 5 as the alignment has "padded" the data to
that position.

#### Syntax:

``` gml
buffer_tell(buffer);
```

|          |                                                                                       |                                 |
|----------|---------------------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                                  | Description                     |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to use. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var pos = buffer_tell(buff); buffer_seek(buff, buffer_seek_start, 0); val[0] = buffer_read(buff, buffer_S16); val[1] = buffer_read(buff, buffer_S16); val[2] = buffer_read(buff, buffer_S16); buffer_seek(buff, buffer_seek_start, pos);
```

The above code will store the current seek position within the buffer
indexed in the variable "buff" to the local variable "pos". The buffer
seek position will then be set to the start of the buffer, and three
pieces of data are read into an array, before finally re-setting the
buffer seek position to where it was previously.
