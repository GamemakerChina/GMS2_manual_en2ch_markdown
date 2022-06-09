# buffer_resize

With this function you can resize a given buffer to be the size (in
bytes) that you specify.

#### Syntax:

``` gml
buffer_resize(buffer, newsize);
```

|          |                                                                                       |                                                |
|----------|---------------------------------------------------------------------------------------|------------------------------------------------|
| Argument | Type                                                                                  | Description                                    |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to change the size of. |
| newsize  |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The new size of the buffer (in bytes).         |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (buffer_get_size(buff) &amp;lt; 16384)
{
    buffer_resize(buff, 16384);
}
```

The above code will check the size of the buffer indexed in the variable
"buff" and if it is less than the given value, the buffer is resized.
