# string_width

This function will return the width (in pixels) of the input string,
taking into account any line-breaks the text may have. It is very handy
for calculating distances between text elements based on the total width
of the letters that make up the string as it would be drawn with [
draw_text() ](../Drawing/Text/draw_text) using the currently defined
font.

#### Syntax:

``` gml
string_width(string);
```

|          |                                                                        |                                     |
|----------|------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                   | Description                         |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to measure the width of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var ww = string_width(str_Name + " "); draw_text(32, 32, str_Name)); draw_text(32 + ww, 32, "has won the game!");
```

The above code will get the width of the given string and then draw two
lines of text, using the returned string width as a separator.
