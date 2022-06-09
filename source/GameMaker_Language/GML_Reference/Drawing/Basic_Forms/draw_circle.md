# draw_circle

With this function you can draw either an outline of a circle or a
filled circle. You can define how precise the drawing is with the
function [ draw_set_circle_precision() ](draw_set_circle_precision)
. **NOTE** : If you are wanting to draw a shape using a shader, you
should be aware that most shaders expect the following inputs: vertex,
texture, Colour. However, when using this function, only vertex and
colour data are being passed in, and so the shader may not draw anything
(or draw something but not correctly). If you need to draw shapes in
this way then the shader should be customised with this in mind.

#### Syntax:

``` gml
draw_circle(x, y, r, outline);
```

|          |                                                                            |                                                                                           |
|----------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                                               |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The x coordinate of the center of the circle.                                             |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The y coordinate of the center of the circle.                                             |
| r        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The circle's radius (length from its center to its edge)                                  |
| outline  |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether the circle is drawn filled ( false ) or as a one pixel wide outline ( true ).     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_colour(c_white);
draw_circle(100, 100, 50, true);
```

This will draw a one pixel wide white circle outline with a radius of 50
pixels.
