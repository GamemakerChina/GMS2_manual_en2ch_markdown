# draw_rectangle

With this function you can draw either an outline of a rectangle or a
filled rectangle where the (x1,y1) position is the top left corner and
the (x2,y2) position is the bottom right corner. Please note that the
rectangle being drawn may need different values (+/-1 on the x, y, or
width or height) to be drawn with the desired dimensions due to
differences across the various supported platforms. **NOTE** : If you
are wanting to draw a shape using a shader, you should be aware that
most shaders expect the following inputs: vertex, texture, Colour.
However, when using this function, only vertex and colour data are being
passed in, and so the shader may not draw anything (or draw something
but not correctly). If you need to draw shapes in this way then the
shader should be customised with this in mind.

#### Syntax:

``` gml
draw_rectangle(x1, y1, x2, y2, outline);
```

|          |                                                                            |                                                                                      |
|----------|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                                          |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The x coordinate of the top left corner of the rectangle.                            |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The y coordinate of the top left corner of the rectangle.                            |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The x coordinate of the bottom right corner of the rectangle.                        |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The y coordinate of the bottom right corner of the rectangle.                        |
| outline  |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether the rectangle is drawn filled (false) or as a one pixel wide outline (true). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_colour(c_yellow);
draw_rectangle(100, 100, 300, 200, true);
```

This will draw a rectangle outline, with its top left corner at
(100,100) and its bottom right corner at (300,200).
