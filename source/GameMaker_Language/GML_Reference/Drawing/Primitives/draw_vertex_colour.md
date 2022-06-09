# draw_vertex_colour

This function defines the position of a vertex for a primitive, with its
own colour and alpha setting. The final look of the primitive will
depend on the primitive type chosen to draw and the order with which you
add the vertexes to it (see [ draw_primitive_begin()
](draw_primitive_begin) for more information) and the vertexes with
different colours and alphas will blend smoothly from one to the other.
To end and draw the primitive you must call [ draw_primitive_end()
](draw_primitive_end) .

#### Syntax:

``` gml
draw_vertex_colour(x, y, col, alpha)
```

|          |                                                                                                           |                                           |
|----------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                                                      | Description                               |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x coordinate of the vertex.           |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y coordinate of the vertex.           |
| col      |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour to draw this vertex with.      |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The alpha to draw this vertex with (0-1). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_primitive_begin(pr_trianglelist); draw_vertex_colour(100, 100, c_blue, 0.1); draw_vertex_colour(100, 200, c_red, 0.1); draw_vertex_colour(150, 150, c_green, 1); draw_primitive_end();
```

The above code will draw a semi-transparent triangle with each vertex
coloured a different colour.
