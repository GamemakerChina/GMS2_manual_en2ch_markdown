# draw_set_font

This function will set the font to be used for all further text drawing.
This font must have been added into the [font
assets](../../../../The_Asset_Editors/Fonts) of the game or have
been created using either the [ font_add ()
](../../Asset_Management/Fonts/font_add) or [ font_add_sprite ()
](../../Asset_Management/Fonts/font_add_sprite) .

#### Syntax:

``` gml
draw_set_font(font);
```

|          |                                                            |                              |
|----------|------------------------------------------------------------|------------------------------|
| Argument | Type                                                       | Description                  |
| font     |  [Font Asset](../../../../../The_Asset_Editors/Fonts)  | The name of the font to use. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_colour(c_blue);
draw_set_font(fnt_Game);
draw_text(200, 200, "Hello World");
```

The above code will draw the given text using the font indexed in the
variable "fnt_Game" and coloured blue.
