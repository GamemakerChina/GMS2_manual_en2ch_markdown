# string_height

This function will return the height (in pixels) of the input string,
taking into account the line separation and any line-breaks the text may
have. It is very handy for calculating distances between text elements
based on the tallest of the letters that make up the string as it would
be drawn with [ draw_text() ](../Drawing/Text/draw_text) using the
currently defined font.

#### Syntax:

``` gml
string_height(string);
```

|          |                                                                        |                                      |
|----------|------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                   | Description                          |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to measure the height of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var hh = string_height("ABCDEFGHIJKLMNOPQRSTUVWXYZ"); draw_text(32, 32, string(score)); draw_text(32, 32 + hh, string(lives);
```

The above code will get the height of the given string and then draw two
lines of text, using the returned string height as a separator.
