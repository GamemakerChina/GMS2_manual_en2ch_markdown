# vertex_normal

This function will add surface normal data to the vertex currently being
defined for the custom primitive. You supply the buffer to write the
data into as well as the x, y and z component parts of the normal.

#### Syntax:

``` gml
vertex_normal(buffer, nx, ny, nz);
```

|          |                                                                                                                   |                                         |
|----------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                              | Description                             |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The buffer to write the information to. |
| nx       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The x component of the surface normal.  |
| ny       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The y component of the surface normal.  |
| nz       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The z component of the surface normal.  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_normal(buff, 0, 1, 1);
```

The above code will set the surface normal of the vertex being defined.
