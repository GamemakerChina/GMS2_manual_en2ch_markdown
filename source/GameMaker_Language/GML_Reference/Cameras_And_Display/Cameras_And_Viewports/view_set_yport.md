# view_set_yport

This function can be used to set the y position of the given view port.
You give the view port index (from 0 to 7) and the new position to place
it at.

#### Syntax:

``` gml
view_set_yport(view_port, y)
```

|           |                                                                         |                                 |
|-----------|-------------------------------------------------------------------------|---------------------------------|
| Argument  | Type                                                                    | Description                     |
| view_port |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The view port to target (0 - 7) |
| y         |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new y position              |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if view_get_yport(0) != (display_get_height() / 2) - (view_hport[0] / 2)
{
    view_set_yport(0, (display_get_height() / 2) - (view_hport[0] / 2));
}
```

The above code will check the y position of the view port\[0\] and if it
is not where it is required to be it is set to that position.
