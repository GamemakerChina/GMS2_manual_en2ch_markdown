# draw_text_transformed

This function will draw text in a similar way to [ draw_text ()
](draw_text) only now you can choose to scale the text along the
horizontal or vertical axis (effectively stretching or shrinking it) and
also have GameMaker draw it at an angle (where 0 is normal and every
degree over 0 rotates the text anti-clockwise).

#### Syntax:

``` gml
draw_text_transformed(x, y, string, xscale, yscale, angle);
```

|          |                                                                           |                                       |
|----------|---------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                      | Description                           |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The x coordinate of the drawn string. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The y coordinate of the drawn string. |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to draw.                   |
| xscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The horizontal scale (default 1).     |
| yscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The vertical scale(default 1).        |
| angle    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The angle of the text.                |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_halign(fa_center); draw_set_valign(fa_middle);
 image_angle += 1; draw_text_transformed(room_width / 2, room_height / 2, "GAME OVER!", 2, 2, image_angle);
```

The above code will draw the given text in the middle of the room,
spinning round and scaled to twice its original size.
