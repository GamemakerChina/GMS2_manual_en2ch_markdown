# vertex_end

With this function you end the building of the custom primitive. Once
you call this command the primitive can be used in the [ vertex_submit()
](vertex_submit) function for use in a shader or you can freeze the
buffer (making the vertex buffer used read-only and much faster) using [
vertex_freeze() ](vertex_freeze) .

#### Syntax:

``` gml
vertex_end(buffer);
```

|          |                                                                                                                   |                               |
|----------|-------------------------------------------------------------------------------------------------------------------|-------------------------------|
| Argument | Type                                                                                                              | Description                   |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The buffer to end writing to. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_end(buff);
```

The above code will end the defining of a custom primitive.
