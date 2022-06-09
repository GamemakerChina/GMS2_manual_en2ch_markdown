# vertex_ubyte4

This function will add four unsigned byte values (0 - 255) to the vertex
data. The vertex must have been formatted correctly to accept this using
the [ vertex_format_add_custom() ](vertex_format_add_custom)
function.

#### Syntax:

``` gml
vertex_ubyte4(buffer, byte, byte, byte, byte);
```

|          |                                                                                                                   |                                         |
|----------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                              | Description                             |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The buffer to write the information to. |
| byte     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The first input value.                  |
| byte     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The second input value.                 |
| byte     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The third input value.                  |
| byte     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The fourth input value.                 |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_ubyte4(buff, irandom(255), irandom(255), irandom(255), 127);
```

The above code will add four values to the vertex data being defined.
