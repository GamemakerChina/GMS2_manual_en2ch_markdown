# vertex_create_buffer_from_buffer_ext

As with the function [ vertex_create_buffer()
](vertex_create_buffer) , this function will create a new vertex
buffer, only now the vertex data it stores is copied from the regular
buffer that is specified as the source. The buffer is pre-formatted with
the vertex format for building primitives for use with (for example)
shaders, and you can also supply an offset within the source buffer to
copy from and the number of vertices that the final buffer should have.
Note that if the number of vertices does not match those being copied
you may get corrupted vertex data.

#### Syntax:

``` gml
vertex_create_buffer_from_buffer_ext(buffer, format, src_offset, vert_num);
```

|            |                                                                                                                          |                                                       |
|------------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument   | Type                                                                                                                     | Description                                           |
| buffer     |  [Buffer ID](../../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                                  | The buffer to create the vertex buffer from.          |
| format     |  [Primitive Type Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/draw_primitive_begin)  | The primitive vertex format to use.                   |
| src_offset |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                   | The offset within the the source buffer to copy from. |
| vert_num   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                   | The number of vertices the buffer should have.        |

#### Returns:

``` gml
 Vertex Buffer ID
```

#### Example:

``` gml
vertex_format_begin();
vertex_format_add_position_3d();
vertex_format_add_colour();
vertex_format_add_textcoord();
var my_format = vertex_format_end();
v_buff = vertex_create_buffer_from_buffer(global.modelBuff, myFormat, 0, 512);
```

The above code will create a new vertex format then create a new vertex
buffer from a previously created regular buffer, applying the custom
vertex format to it with 0 offset. The function tells the new vertex
buffer that it should expect 512 vertices.
