# view_get_yport

This function can be used to retrieve the y position of the given view
port.

#### Syntax:

``` gml
view_get_yport(view_port)
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
if view_get_yport(0) != (display_get_height() / 2) - (view_hport[0] / 2)
{
    view_set_yport(0, (display_get_height() / 2) - (view_hport[0] / 2));
}
```

The above code will check the y position of the view port\[0\] and if it
is not where it is required to be it is set to that position.
