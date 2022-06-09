# view_get_visible

This function can be used to check the visibility of the given view
port. The function will return true if it is visible and false if it is
not.

#### Syntax:

``` gml
view_get_visible(view_port)
```

|           |                                                                         |                                 |
|-----------|-------------------------------------------------------------------------|---------------------------------|
| Argument  | Type                                                                    | Description                     |
| view_port |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The view port to target (0 - 7) |

#### Returns:

``` gml
 Boolean
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
