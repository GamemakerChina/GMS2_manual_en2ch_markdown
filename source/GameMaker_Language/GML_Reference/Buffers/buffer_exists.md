# buffer_exists

This function can be used to check a variable to see if it holds a valid
buffer ID value or not. If it does the function will return true
otherwise it will return false .

#### Syntax:

``` gml
buffer_exists(buffer)
```

|          |                                                                                       |                                   |
|----------|---------------------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                                  | Description                       |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if buffer_exists(buff)
{
    buffer_delete(buff);
}
```

The above code checks to see if the variable " buff " holds a buffer ID
and if it does, the buffer is deleted.
