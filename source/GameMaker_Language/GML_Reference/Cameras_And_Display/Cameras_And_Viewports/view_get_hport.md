# view_get_hport

This function can be used to retrieve the height of the given view port.

#### Syntax:

``` gml
view_get_hport(view_port)
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
if view_get_hport(0) != (display_get_height () / 2)
{
    view_set_hport(0, display_get_height() / 2);
}
```

The above code will check the height of the view port\[0\] and if it is
not half of the display height it is set to that value.
