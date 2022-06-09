# buffer_compress

With this function you can compress part (or all) of a buffer using
[zlib compression](https://en.wikipedia.org/wiki/Zlib) . You supply the
ID of the buffer to compress (as returned by [ buffer_create()
](buffer_create) ), the offset within the buffer to use in bytes,
and the size of the buffer data to compress (also in bytes). The
function will return a new buffer ID value for the compressed buffer, or
a value less than 0 if it has failed for any reason. This function will
not alter the original buffer.

#### Syntax:

``` gml
buffer_compress(buffer, offset, size);
```

|          |                                                                                       |                                                      |
|----------|---------------------------------------------------------------------------------------|------------------------------------------------------|
| Argument | Type                                                                                  | Description                                          |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to compress.                 |
| offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The offset within the buffer to compress (in bytes). |
| size     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The size of the buffer area to compress (in bytes).  |

#### Returns:

``` gml
 Buffer ID
```

#### Example:

``` gml
var srcBuff = buffer_create(1024, buffer_grow, 1);
buffer_write(srcBuff, global.DataString);
var cmpBuff = buffer_compress(srcBuff, 0, buffer_tell(srcBuff));
buffer_save(cmpBuff, "Player_Save.sav");
buffer_delete(srcBuff);
buffer_delete(cmpBuff);
```

The above code will create a buffer then populate it with the data from
a string. This buffer is then compressed and saved, and both the source
and compressed buffers are deleted
