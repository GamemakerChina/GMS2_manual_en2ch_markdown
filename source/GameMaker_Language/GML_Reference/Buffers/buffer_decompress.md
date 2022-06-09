# buffer_decompress

With this function you can decompress a previously compressed buffer
using [zlib compression](https://en.wikipedia.org/wiki/Zlib) . You
supply the buffer ID to decompress, and the function will return a new
buffer ID that contains the uncompressed data. If the decompression has
failed (for example, you are supplying a buffer that hasn't been
compressed) then the function will instead return a value less than 0.

#### Syntax:

``` gml
buffer_decompress(buffer);
```

|          |                                                                                       |                                        |
|----------|---------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                  | Description                            |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to decompress. |

#### Returns:

``` gml
 Buffer ID
```

#### Example:

``` gml
var cmpBuff = buffer_load("Player_Save.sav");
var srcBuff = buffer_decompress(cmpBuff);
global.DataString = buffer_read(srcBuff, buffer_string);
```

The above code will first load a saved buffer, then decompress it and
finally read the string data from the decompressed buffer into a global
variable.
