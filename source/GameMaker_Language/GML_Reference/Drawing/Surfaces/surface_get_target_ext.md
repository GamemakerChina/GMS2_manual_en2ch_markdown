# surface_get_target_ext

This function will retrieve the surface ID assigned to one of the 4
render targets available to surfaces. You supply the index of the render
target to check, and the function will return -1 if no surface is
assigned, or an integer value \>= 0, representing the ID of the surface
assigned (as returned by the function [ surface_create()
](surface_create) ).

#### Syntax:

``` gml
surface_get_target_ext(index);
```

|          |                                                                         |                                                 |
|----------|-------------------------------------------------------------------------|-------------------------------------------------|
| Argument | Type                                                                    | Description                                     |
| index    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The render target index to check (from 0 to 3). |

#### Returns:

``` gml
 Surface ID

or -1 (if no target surface is set)
```

#### Example:

``` gml
if surface_get_target_ext(0) == -1
{
    surface_set_target_ext(0, global.Surf);
}
```

The above code will first check and see if the shader render target 0
has been set to a surface, and if not, then one is assigned.
