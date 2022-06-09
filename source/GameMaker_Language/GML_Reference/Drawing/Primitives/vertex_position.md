# vertex_position

This function will add 2D position data to the vertex currently being
defined for the custom primitive. You supply the buffer to write the
data into as well as the x and y position for drawing.

#### Syntax:

``` gml
vertex_position(buffer, x, y);
```

|          |                                                                                                                   |                                         |
|----------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                              | Description                             |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The buffer to write the information to. |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The x position.                         |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The y position.                         |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_position(buff, x - 100, y - 125);
```

The above code will set the position of the vertex being defined.
