# vertex_float1

This function will add a floating point value to the vertex data. The
vertex must have been formatted correctly to accept this using the [
vertex_format_add_custom() ](vertex_format_add_custom) function.

#### Syntax:

``` gml
vertex_float1(buffer, float);
```

|          |                                                                                                                   |                                         |
|----------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                              | Description                             |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The buffer to write the information to. |
| float    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The input value.                        |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_float1(buff, 0.05);
```

The above code will add a floating point value to the vertex data being
defined.
