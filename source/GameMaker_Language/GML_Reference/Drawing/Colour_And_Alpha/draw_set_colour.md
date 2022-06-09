# draw_set_colour

With this function you can set the base draw colour for the game. This
will affect drawing of fonts, forms, primitives and 3D, however it will
not affect sprites (drawn
[manually](../Sprites_And_Tiles/draw_sprite) or by an instance). If
any affected graphics are drawn with their own colour values, this value
will be ignored.

#### Syntax:

``` gml
draw_set_colour(col);
```

|          |                                                                                                           |                                |
|----------|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                                                      | Description                    |
| col      |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour to set for drawing. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_alpha(0.5);
draw_set_colour(c_black);
draw_text(x+5, y+5, "LEVEL 1");
draw_set_alpha(1);
draw_set_colour(c_white);
draw_text(x, y, "LEVEL 1");
```

The above code will draw some text at the specified position with a
shadow effect created by modified draw alpha and colour.
