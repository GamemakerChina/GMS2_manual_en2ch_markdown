# vertex_format_delete

This function must be called whenever you are finished using any created
vector formats. You provide the format ID value (as returned by the
function [ vector_format_end() ](vertex_format_end) ), and this
function will free the memory associated with it. Note that if you try
to use this format again after calling this function, you will get an
error.

#### Syntax:

``` gml
vertex_format_delete(formatID);
```

|          |                                                                                                                |                             |
|----------|----------------------------------------------------------------------------------------------------------------|-----------------------------|
| Argument | Type                                                                                                           | Description                 |
| formatID |  [Vertex Format ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_format_end)  | The vertex format to delete |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_format_delete(myFormat);
```

The above code will remove the vertex format created in the variable
"myFormat" from memory.
