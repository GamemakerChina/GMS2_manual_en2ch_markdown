# vertex_delete_buffer

This function can be used to remove a previously created vertex buffer
(see [ vertex_create_buffer() ](vertex_create_buffer) ) from system
memory. This will also remove all vertex data for any custom primitives
that it contained.

#### Syntax:

``` gml
vertex_delete_buffer(buffer);
```

|          |                                                                                                                   |                                  |
|----------|-------------------------------------------------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                                                              | Description                      |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The vertex buffer to be removed. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_delete_buffer(v_buff);
```

The above code will delete from memory the buffer indexed in the
variable "v_buff".
