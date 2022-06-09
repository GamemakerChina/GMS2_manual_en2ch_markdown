# vertex_texcoord

This function will set the texture coordinates to use for the vertex
currently being defined for the custom primitive. You supply the buffer
to write the data into as well as the UV position within the texture to
use.

#### Syntax:

``` gml
vertex_texcoord(buffer, u, v);
```

|          |                                                                                                                   |                                               |
|----------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Argument | Type                                                                                                              | Description                                   |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The buffer to write the information to.       |
| u        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The first texture coordinate to use (0 - 1).  |
| v        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The second texture coordinate to use (0 - 1). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_texcoord(buff, 0, 0);
```

The above code will set the UV values of the vertex being defined.
