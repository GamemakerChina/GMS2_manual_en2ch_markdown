# view_set_visible

This function can be used to set the visibility of the given view port.
The function takes the view port index (from 0 to 7) and a boolean true
if it is visible and false if it is not.

#### Syntax:

``` gml
view_set_visible(view_port, visible)
```

|           |                                                                            |                                                                 |
|-----------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument  | Type                                                                       | Description                                                     |
| view_port |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The view port to target (0 - 7)                                 |
| visible   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Visibility toggle ( true is visible and false is invisible)     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if !view_get_visible(0)
{
    view_set_visible(0, true);
}
```

The above code will check to see if the view port\[0\] is visible and if
it is not it is set to visible.
