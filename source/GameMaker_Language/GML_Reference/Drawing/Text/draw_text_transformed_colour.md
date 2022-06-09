# draw_text_transformed_colour

This function is a combination of the base [ draw_text()
](draw_text) function with the [ draw_text_transformed()
](draw_text_transformed) and [ draw_text_colour()
](draw_text_colour) functions, permitting you to scale and rotate
text as well as colour it with a gradient fill and change its alpha
value, ignoring the base alpha and colour settings for drawing. ** NOTE
** Gradient blending is not available for the HTML5 target unless WebGL
is enabled, although you can still set the blending colours and it will
blend the font with the first given colour. However all blending in this
way creates a duplicate font which is then stored in the cache and used
when required, which is far from optimal and if you use multiple colour
changes it will slow down your games performance. You can set the font
cache size to try and limit this should it be necessary using the
function [ font_set_cache_size()
](../../Asset_Management/Fonts/font_set_cache_size) .

#### Syntax:

``` gml
draw_text_transformed_colour(x, y, string, xscale, yscale, angle, c1, c2, c3, c4, alpha);
```

|          |                                                                                                           |                                                    |
|----------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| Argument | Type                                                                                                      | Description                                        |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x coordinate of the drawn string.              |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y coordinate of the drawn string.              |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                  | The string to draw.                                |
| xscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The horizontal scale.                              |
| yscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The vertical scale.                                |
| angle    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The angle of the text.                             |
| c1       |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour for the top left of the drawn text.     |
| c2       |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour for the top right of the drawn text.    |
| c3       |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour for the bottom right of the drawn text. |
| c4       |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour for the bottom left of the drawn text.  |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The alpha for the text.                            |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_halign(fa_center); draw_set_valign(fa_middle);
 image_angle += 1; draw_text_transformed_colour(room_width / 2, room_height / 2, keyboard_string, 2, 2, image_angle, c_red, c_red, c_yellow, c_yellow, 0.5);
```

The above code will draw the given text in the middle of the room,
spinning round and scaled to twice its original size, with a colour
gradient going from yellow to red as well as an alpha of 0.5.
