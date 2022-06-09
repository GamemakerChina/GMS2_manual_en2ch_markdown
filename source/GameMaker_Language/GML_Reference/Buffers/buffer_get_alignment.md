# buffer_get_alignment

With this function you can get the a *byte alignment* for the given
buffer ID.

#### Syntax:

``` gml
buffer_get_alignment(buffer);
```

|          |                                                                                       |                                   |
|----------|---------------------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                                  | Description                       |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
alignment = buffer_get_alignment(buff);
```

The above code will get the alignment of the buffer from the value
indexed in the variable "buff" and store it in a variable.
