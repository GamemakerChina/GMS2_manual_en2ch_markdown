# view_get_surface_id

This function can be used to retrieve the unique ID value for the
surface assigned to the given view port (will return -1 if no surface
has been assigned).

#### Syntax:

``` gml
view_get_surface_id(view_port)
```

|           |                                                                         |                                 |
|-----------|-------------------------------------------------------------------------|---------------------------------|
| Argument  | Type                                                                    | Description                     |
| view_port |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The view port to target (0 - 7) |

#### Returns:

``` gml
 Surface ID
```

#### Example:

``` gml
if view_get_surface_id(0) == -1
{
    view_set_surface_id(0, global.vSurf);
}
```

The above code will check to see if a surface has been assigned to the
view port\[0\] and if it has not then one is assigned.
