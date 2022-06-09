# draw_roundrect_colour_ext

With this function you can draw either an outline of a rounded rectangle
or a filled rounded rectangle where the (x1,y1) position is the top left
corner and the (x2,y2) position is the bottom right corner. If the
rectangle is filled, then the colour arguments will be used to generate
a colour gradient from the centre to the edges, where colour 1 is the
centre colour and colour 2 the edge colour. You must also supply radius
values for the x and y axis (in pixels) and the corners will be rounded
by these amounts. You can define how precise the drawing of the corners
is with the function [ draw_set_circle_precision()
](draw_set_circle_precision) . Please note that the rectangle being
drawn may need different values (+/-1 on the x, y, or width or height)
to be drawn with the desired dimensions due to differences across the
various supported platforms. **NOTE** : If you are wanting to draw a
shape using a shader, you should be aware that most shaders expect the
following inputs: vertex, texture, Colour. However, when using this
function, only vertex and colour data are being passed in, and so the
shader may not draw anything (or draw something but not correctly). If
you need to draw shapes in this way then the shader should be customised
with this in mind.

#### Syntax:

``` gml
draw_roundrect_colour_ext(x1, y1, x2, y2, xrad, yrad, col1, col2, outline);
```

|          |                                                                                                           |                                                                      |
|----------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Argument | Type                                                                                                      | Description                                                          |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x coordinate of the left of the rounded rectangle.               |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y coordinate of the top of the rounded rectangle.                |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x coordinate of the right of the rounded rectangle.              |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y coordinate of the bottom of the rounded rectangle.             |
| xrad     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The radius of the curve along the x axis from the rectangle corners. |
| yrad     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The radius of the curve along the y axis from the rectangle corners. |
| col1     |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The center colour.                                                   |
| col2     |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The outside edge colour.                                             |
| outline  |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | Whether the rectangle is an outline (true) or filled in (false).     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var dist = point_distance(x, y, mouse_x, mouse_y) / 10;
var col = make_colour_hsv(clamp(dist, 0, 255), 255, 255);
draw_roundrect_colour_ext(x - 50, y - 50, x + 50, y + 50, dist, dist, col, c_white, 0);
```

This would draw a filled-in square with rounded corners, the radius of
which is defined by the distance from the instance doing the drawing to
the mouse. This value is also used to calculate the centre blend colour.
