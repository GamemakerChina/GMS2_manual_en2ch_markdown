# vertex_get_number

With this function you can find out the number of individual vertices
defined in any given vertex buffer.

#### Syntax:

``` gml
vertex_get_number(buffer);
```

|          |                                                                                                                   |                             |
|----------|-------------------------------------------------------------------------------------------------------------------|-----------------------------|
| Argument | Type                                                                                                              | Description                 |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The vertex buffer to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
v_num = vertex_get_number(v_buffer);
```

The above code will store the number of vertices stored in the given
vertex buffer to a variable.
