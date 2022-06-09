# view_set_xport

This function can be used to set the x position of the given view port.
You give the view port index (from 0 to 7) and the new position to place
it at.

#### Syntax:

``` gml
view_set_xport(view_port, x)
```

|           |                                                                         |                                 |
|-----------|-------------------------------------------------------------------------|---------------------------------|
| Argument  | Type                                                                    | Description                     |
| view_port |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The view port to target (0 - 7) |
| x         |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new x position              |

#### Returns:

``` gml
N/A
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
