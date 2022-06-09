# draw_text

With this function you can draw any string at any position within the
room (for drawing real numbers you should use the [ string ()
](../../Strings/string) function to convert them into text). To
combine strings you can use **+** (see example below) and you can also
use **\n** within a string to add a line break so it is drawn over
multiple lines (for information on how to properly format a string and
what escape characters you can use, please see
[here](../../Strings/Strings) ). The colour of the text and the
alpha are governed by the current base alpha and colour values as set by
[ draw_set_alpha () ](../Colour_And_Alpha/draw_set_alpha) and [
draw_set_colour () ](../Colour_And_Alpha/draw_set_colour) . **NOTE**
: The actual position of the text will be influenced by the alignment
values set by [ draw_set_halign () ](draw_set_halign) and [
draw_set_valign () ](draw_set_valign) .

#### Syntax:

``` gml
draw_text(x, y, string);
```

|          |                                                                           |                                       |
|----------|---------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                      | Description                           |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The x coordinate of the drawn string. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The y coordinate of the drawn string. |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to draw.                   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_text(x, y, "Hello, " + global.Name + "!\nI hope you are well!");
```

The above code will draw a string at the instance x/y position, which
will use the string stored in the global variable "Name" and split it
over two lines.
