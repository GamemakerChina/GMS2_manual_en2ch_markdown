# draw_arrow

This function will draw an arrow from point (x1,y1) to point (x2,y2).
The stem of the arrow is drawn along these points with the actual arrow
head being drawn at the end, where the size of the arrowhead is defined
by the argument "size" and is calculated as being part of the stem so
that the end point is always aligned with the position defined by x2,y2.
The width of the arrow head is calculated automatically in proportion to
the length. **NOTE** : If you are wanting to draw a shape using a
shader, you should be aware that most shaders expect the following
inputs: vertex, texture, Colour. However, when using this function, only
vertex and colour data are being passed in, and so the shader may not
draw anything (or draw something but not correctly). If you need to draw
shapes in this way then the shader should be customised with this in
mind.

#### Syntax:

``` gml
draw_arrow(x1, y1, x2, y2, size);
```

|          |                                                                         |                                                                     |
|----------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                         |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the start of the line.                          |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the start of the line.                          |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the end of the line (where the arrowhead ends). |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the end of the line (where the arrowhead ends). |
| size     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The length of the arrow in pixels.                                  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_arrow(x, y, mouse_x, mouse_y, 10);
```

The above code will draw an arrow from the position of the instance to
the position of the mouse, with the arrow head being 10 pixels long.
