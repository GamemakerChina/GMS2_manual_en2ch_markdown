# vertex_create_buffer

With this function you can create a new vertex buffer. This is a special
*grow* buffer created by GameMaker which is pre-formatted for use when
building primitives (for use with shaders, for example). The function
will return an index for the buffer which should then be used in all
further calls to it. When using a vertex buffer created with this
function you simply call [ vertex_begin() ](vertex_begin) to start
assigning vertex data to it to start to define your custom primitive,
which will then be held in the buffer ready for submission to the
shader. The buffer can be re-used when necessary (unless you have used
the [ vertex_freeze() ](vertex_freeze) function), with each call of
[ vertex_begin() ](vertex_begin) wiping the previous buffer data
ready to accept the new data.

#### Syntax:

``` gml
vertex_create_buffer();
```

#### Returns:

``` gml
 Vertex Buffer ID
```

#### Example:

``` gml
v_buff = vertex_create_buffer();
```

The above code will create a new a new vertex buffer and store its
handle in the variable "v_buff".
