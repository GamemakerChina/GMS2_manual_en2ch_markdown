# view_set_wport

This function can be used to set the width of the given view port. You
give the view port index (from 0 to 7) and the new width to use.

#### Syntax:

``` gml
view_set_wport(view_port, w)
```

|           |                                                                         |                                 |
|-----------|-------------------------------------------------------------------------|---------------------------------|
| Argument  | Type                                                                    | Description                     |
| view_port |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The view port to target (0 - 7) |
| w         |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new width (in pixels)       |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if view_get_wport(0) != (display_get_width () / 2)
{
    view_set_wport(0, display_get_width() / 2);
}
```

The above code will check the width of the view port\[0\] and if it is
not half of the display width it is set to that value.
