# draw_text_ext_transformed

This function is a combination of the base [ draw_text ()
](draw_text) function with the [ draw_text_ext ()
](draw_text_ext) and [ draw_text_transformed ()
](draw_text_transformed) functions, permitting you to scale and
rotate text while maintaining a specific line spacing and maximum width
per line. Note that the "width" argument is based on a scale of 1, so if
the scale is different, this value should be changed proportionally. For
example, if the base width for a line break is 300 and you set the scale
to 2, then the text will appear wrong, over-running the given width.
Instead you should have set the width to 150 to compensate the scaling.

#### Syntax:

``` gml
draw_text_ext_transformed(x, y, string, sep, w, xscale, yscale, angle);
```

|          |                                                                           |                                                                |
|----------|---------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                      | Description                                                    |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The x coordinate of the drawn string.                          |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The y coordinate of the drawn string.                          |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to draw.                                            |
| sep      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The distance in pixels between lines of text.                  |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The maximum width in pixels of the string before a line break. |
| xscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The horizontal scale.                                          |
| yscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The vertical scale.                                            |
| angle    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The angle of the text.                                         |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_halign(fa_center); draw_set_valign(fa_middle);
 image_angle += 1; draw_text_ext_transformed(room_width / 2, room_height / 2, keyboard_string, 10, 300, 2, 2, image_angle);
```

The above code will draw the given text in the middle of the room, with
a maximum string length of 300 pixels, a spacing between each line of 10
pixels, spinning round and scaled to twice its original size.
