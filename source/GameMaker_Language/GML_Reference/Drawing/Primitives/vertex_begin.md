# vertex_begin

With this function you begin the definition of a custom primitive. You
assign a buffer to write the primitive to, and the vertex format to use
(previously defined using the vertex format functions). You would then
define the necessary points for each vertex of the primitive before
calling [ vertex_end() ](vertex_end) to finalise the primitive
creation.

#### Syntax:

``` gml
vertex_begin(buffer, format);
```

|          |                                                                                                                   |                              |
|----------|-------------------------------------------------------------------------------------------------------------------|------------------------------|
| Argument | Type                                                                                                              | Description                  |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The buffer to be written to. |
| format   |  [Vertex Format ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_format_end)     | The vertex format to use.    |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_format_begin();
vertex_format_add_position();
vertex_format_add_colour();
vertex_format_add_textcoord();
v_format = vertex_format_end();
v_buff = vertex_create_buffer();
vertex_begin(v_buff, v_format);
```

The above code will define a new vertex format, create a new buffer and
start the definition process of a new primitive.
