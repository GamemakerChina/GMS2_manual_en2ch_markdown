# draw_point_colour

With this function you can draw a single pixel anywhere on the screen
with a colour that you define. The colour settings will over-ride the
base colour set with the function [ draw_set_colour()
](../Colour_And_Alpha/draw_set_colour) . **NOTE** : If you are
wanting to draw a shape using a shader, you should be aware that most
shaders expect the following inputs: vertex, texture, Colour. However,
when using this function, only vertex and colour data are being passed
in, and so the shader may not draw anything (or draw something but not
correctly). If you need to draw shapes in this way then the shader
should be customised with this in mind.

#### Syntax:

``` gml
draw_point_colour(x, y, col1);
```

|          |                                                                                                           |                                |
|----------|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                                                      | Description                    |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x coordinate of the point. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y coordinate of the point. |
| col1     |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour of the point.       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_point_colour(50, 50, c_red);
```

This would draw a red pixel at (50,50).
