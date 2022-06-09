# draw_get_font

This function will get the font currently assigned for drawing text. The
function will return -1 if no font is set, or the ID value (a positive
integer) for the font asset assigned.

#### Syntax:

``` gml
draw_get_font();
```

#### Returns:

``` gml
 Font Asset

or -1
```

#### Example:

``` gml
var _cur_font = draw_get_font();
var _y_offset = 0;

switch (_cur_font)
{
    case ft_small:
        _y_offset = 10;
    break;

    case ft_medium:
        _y_offset = 22;
    break;

    case ft_big:
        _y_offset = 34;
    break;

    default:
        _y_offset = 8;
}

draw_text(room_width / 2, 200 + _y_offset, "MENU");
```

The above code gets the currently applied font and runs a switch
statement on it, applying a different Y offset value depending on the
font. It then uses that offset value while drawing some text.
