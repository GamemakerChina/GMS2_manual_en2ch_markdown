# vertex_get_buffer_size

With this function you can get the size of the given vertex buffer in
bytes.

#### Syntax:

``` gml
vertex_get_buffer_size(buffer);
```

|          |                                                                                                                   |                                |
|----------|-------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                                                              | Description                    |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The buffer to get the size of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
bufferBytes = vertex_get_buffer_size(buff);
```

The above code will get the number of bytes used by the vertex buffer
given and store the value in the variable "bufferBytes".
