# draw_vertex

This function defines the position of a vertex for a primitive. The
final look of the primitive will depend on the primitive type chosen to
draw and the order with which you add the vertexes to it. See
[draw_primitive_begin()](draw_primitive_begin) for more information.
To end and draw the primitive you must call [ draw_primitive_end()
](draw_primitive_end) .

#### Syntax:

``` gml
draw_vertex(x, y)
```

|          |                                                                         |                                 |
|----------|-------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                    | Description                     |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the vertex. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the vertex. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_primitive_begin(pr_trianglelist); draw_vertex(100, 100); draw_vertex(100, 200); draw_vertex(150, 150); draw_primitive_end();
```

The above code will draw a simple triangle primitive.
