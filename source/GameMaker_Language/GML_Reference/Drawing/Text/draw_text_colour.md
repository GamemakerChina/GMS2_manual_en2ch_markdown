# draw_text_colour

This function will draw text in a similar way to [ draw_text ()
](draw_text) only now you can choose the colours to use for
colouring the text as well as the alpha value, and these new values will
be used instead of the base drawing colour and alpha. **NOTE** :
Gradient blending is not available for the HTML5 target unless WebGL is
enabled, although you can still set the blending colours and it will
blend the font with the first given colour. However all blending in this
way creates a duplicate font which is then stored in the cache and used
when required, which is far from optimal and if you use multiple colour
changes it will slow down your games performance. You can set the font
cache size to try and limit this should it be necessary using the
function [ font_set_cache_size()
](../../Asset_Management/Fonts/font_set_cache_size) .

#### Syntax:

``` gml
draw_text_colour(x, y, string, c1, c2, c3, c4, alpha);
```

|          |                                                                                                           |                                                    |
|----------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| Argument | Type                                                                                                      | Description                                        |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x coordinate of the drawn string.              |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y coordinate of the drawn string.              |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                  | The string to draw.                                |
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
draw_set_colour(c_white); draw_text(100, 100, "Health"); draw_text_colour(100, 200, string(health), c_lime, c_lime, c_green, c_green, 1);
```

The above code will draw two sections of text on the same line, with the
first text being drawn white (as that is the base drawing colour) and
the second text being drawn with a lime green to normal green gradient.
