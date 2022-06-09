# vertex_create_buffer_ext

As with the function [ vertex_create_buffer()
](vertex_create_buffer) , this function will create a new vertex
buffer. This is a special *grow* buffer created by GameMaker which is
pre-formatted for use when building primitives for use with shaders. You
can specify an initial starting size for the buffer (in bytes) and it
will return an index for the buffer which should then be used in all
further calls to the buffer.

#### Syntax:

``` gml
vertex_create_buffer_ext(size);
```

|          |                                                                         |                                            |
|----------|-------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                    | Description                                |
| size     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The initial size of the buffer (in bytes). |

#### Returns:

``` gml
 Vertex Buffer ID
```

#### Example:

``` gml
v_buff = vertex_create_buffer_ext(1024 * 1024);
```

The above code will create a new vertex buffer, initially 1MB in size,
and store its handle in the variable "v_buff".
