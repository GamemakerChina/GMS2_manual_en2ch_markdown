# view_set_hport

This function can be used to set the height of the given view port. You
give the view port index (from 0 to 7) and the new height to use.

#### Syntax:

``` gml
view_set_hport(view_port, h)
```

|           |                                                                         |                                 |
|-----------|-------------------------------------------------------------------------|---------------------------------|
| Argument  | Type                                                                    | Description                     |
| view_port |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The view port to target (0 - 7) |
| h         |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new height (in pixels)      |

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
