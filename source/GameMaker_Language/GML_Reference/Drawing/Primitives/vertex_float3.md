# vertex_float3

This function will add three floating point values to the vertex data.
The vertex must have been formatted correctly to accept this using the [
vertex_format_add_custom() ](vertex_format_add_custom) function.

#### Syntax:

``` gml
vertex_float3(buffer, float, float, float);
```

|          |                                                                                                                   |                                         |
|----------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                              | Description                             |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The buffer to write the information to. |
| float    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The first input value.                  |
| float    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The second input value.                 |
| float    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The third input value.                  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_float3(buff, 0.05, 0.01, room_width / x);
```

The above code will add three floating point values to the vertex data
being defined.
