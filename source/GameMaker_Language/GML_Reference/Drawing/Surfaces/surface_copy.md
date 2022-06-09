# surface_copy

This function simply takes the image from one surface and copies it onto
another one at the specified local position within that surface (where
the (0,0) position is the top left corner of the destination surface).
If the destination surface already has information this will be
overwritten by the copy, and the function does *not* change the source
surface in any way. **NOTE** : When working with surfaces there is the
possibility that they can cease to exist at any time due to them being
stored in texture memory. You should **ALWAYS** check that a surface
exists using [ surface_exists() ](surface_exists) before referencing
them directly.

#### Syntax:

``` gml
surface_copy(destination, x, y, source);
```

|             |                                                                                                     |                                                     |
|-------------|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument    | Type                                                                                                | Description                                         |
| destination |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of the surface to copy the other surface to. |
| x           |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The x position to copy to.                          |
| y           |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The y position to copy to.                          |
| source      |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of surface to be copied.                     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if view_current == 0
{
    surface_copy(surf, 0, 0, temp_surf);
}
else
{
    draw_surface(surf, 0, 0);
}
```

The above code will check the current view being drawn and if it is
view\[0\] it copies the surface indexed in the variable "temp_surf" onto
the surface indexed in the variable "surf". If the current view is
anything other than view\[0\] the surface "surf" is drawn to the screen.
