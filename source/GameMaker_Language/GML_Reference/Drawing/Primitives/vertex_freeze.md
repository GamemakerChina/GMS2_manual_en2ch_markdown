# vertex_freeze

This function can be used to "freeze" a vertex buffer. This buffer
becomes **read-only** , meaning that should you need to change it, you
would have to delete the whole buffer and re-create it. A frozen buffer
can be submitted to the shader faster than a normal, dynamic buffer and
is recommended for those effects that require an unchanging custom
primitive for the duration of a level or the game. The function will
return 0 on successfully freezing the specified vertex buffer, however
if it failed for any reason, it will return -1.

#### Syntax:

``` gml
vertex_freeze(buffer);
```

|          |                                                                                                                   |                              |
|----------|-------------------------------------------------------------------------------------------------------------------|------------------------------|
| Argument | Type                                                                                                              | Description                  |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The vertex buffer to freeze. |

#### Returns:

``` gml
 Real

(0 for success, -1 for failure)
```

#### Example:

``` gml
// Create event
vertex_freeze(vbuff);
```

The above code will freeze the given vertex buffer in the Create event,
so it can be used as a "static" buffer in other events for faster
access.
