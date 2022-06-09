# view_get_xport

This function can be used to retrieve the x position of the given view
port.

#### Syntax:

``` gml
view_get_xport(view_port)
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
if view_get_xport(0) != (display_get_width() / 2) - (view_wport[0] / 2)
{
    view_set_xport(0, (display_get_width() / 2) - (view_wport[0] / 2));
}
```

The above code will check the x position of the view port\[0\] and if it
is not where it is required to be it is set to that position.
