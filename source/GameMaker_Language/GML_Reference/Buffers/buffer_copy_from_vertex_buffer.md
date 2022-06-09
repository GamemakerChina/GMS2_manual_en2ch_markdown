# buffer_copy_from_vertex_buffer

This function can be used to copy some (or all) of the vertex data
stored in one vertex buffer into a previously created regular buffer.
When copying from a vertex buffer into a regular buffer with this
function, both buffers must have previously been created (using the [
vertex_create_buffer() ](../Drawing/Primitives/vertex_create_buffer)
and [ buffer_create() ](buffer_create) functions, for example). You
can specify the range of vertex data that you wish to copy into the
buffer, where the start vertex can be anywhere between 0 and the number
of vertices -1, and you can give the number of vertices from that point
on to copy. You can use the function [ vertex_get_number()
](../Drawing/Primitives/vertex_get_number) on the vertex buffer to
get the total number of vertices stored. Finally you give the buffer
index to copy the vertex data into, as well as a data offset to define
the position to copy the vertex data to in the destination buffer.

#### Syntax:

``` gml
buffer_copy_from_vertex_buffer(vertex_buffer, start_vertex, num_vertices, dest_buffer, dest_offset);
```

|               |                                                                                                                |                                                     |
|---------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument      | Type                                                                                                           | Description                                         |
| vertex_buffer |  [Vertex Buffer ID](../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The index of the vertex buffer to copy *from* .     |
| start_vertex  |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The starting vertex.                                |
| num_vertices  |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The total number of vertices to use.                |
| dest_buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                           | The index of the buffer to copy *to* .              |
| dest_offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The offset position to copy the data to (in bytes). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var v_num = vertex_get_number(model_buff); buffer_copy_from_vertex_buffer(model_buffer, 0, v_num - 1, player_buffer, 0);
```

The above code will copy the vertex data stored in the vertex buffer
indexed in the variable "model_buffer", and then paste it into the
buffer indexed in the variable "player_buffer".
