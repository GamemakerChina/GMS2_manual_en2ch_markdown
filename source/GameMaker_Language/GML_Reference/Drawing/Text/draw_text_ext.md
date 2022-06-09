# draw_text_ext

This function will draw text in a similar way to [ draw_text ()
](draw_text) only now you can set the space between each line of
text - should the text occupy more than one line - and limit the width
(in pixels) of the string per line so that should any line exceed this
value, GameMaker will automatically split the text to the next line at
the nearest available white-space (if the text has no white-spaces then
it will overrun this maximum width value). Note that any white space
placed at the start of the string will be stripped out before being
parsed for drawing because of this. Also note that a value of -1 for the
line separation argument will default to a separation based on the
height of the "M" character in the chosen font.

#### Syntax:

``` gml
draw_text_ext(x, y, string, sep, w);
```

|          |                                                                           |                                                                |
|----------|---------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                      | Description                                                    |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The x coordinate of the drawn string.                          |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The y coordinate of the drawn string.                          |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to draw.                                            |
| sep      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The distance in pixels between lines of text.                  |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The maximum width in pixels of the string before a line break. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_text_ext(100, 50, keyboard_string, 3, 300);
```

The above code will draw whatever text the user types into the keyboard,
splitting it onto new lines every time the string length for that line
exceeds 300 pixels. the code will also maintain a separation of 3 pixels
between lines should this occur.
