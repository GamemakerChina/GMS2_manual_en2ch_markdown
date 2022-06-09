# vertex_create_buffer_from_buffer

As with the function [ vertex_create_buffer()
](vertex_create_buffer) , this function will create a new vertex
buffer, only now the vertex data it stores is copied from the regular
buffer that is specified as the source. The buffer created is a special
*grow* buffer which is pre-formatted with the vertex format for building
primitives for use with (for example) shaders. This function requires
that you supply the pointer to a previously created regular buffer, and
a vertex format that should be applied to the copied data.

#### Syntax:

``` gml
vertex_create_buffer_from_buffer(buffer, format);
```

|          |                                                                                                                          |                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                                     | Description                                  |
| buffer   |  [Buffer ID](../../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                                  | The buffer to create the vertex buffer from. |
| format   |  [Primitive Type Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/draw_primitive_begin)  | The primitive vertex format to use.          |

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
v_buff = vertex_create_buffer_from_buffer(global.modelBuff, myFormat);
```

The above code will create a new vertex format then create a new vertex
buffer from a previously created regular buffer, applying the custom
vertex format to it.
