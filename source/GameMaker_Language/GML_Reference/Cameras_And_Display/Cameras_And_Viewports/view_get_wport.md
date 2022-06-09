# view_get_wport

This function can be used to retrieve the width of the given view port.

#### Syntax:

``` gml
view_get_wport(view_port)
```

|           |                                                                         |                                 |
|-----------|-------------------------------------------------------------------------|---------------------------------|
| Argument  | Type                                                                    | Description                     |
| view_port |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The view port to target (0 - 7) |

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
