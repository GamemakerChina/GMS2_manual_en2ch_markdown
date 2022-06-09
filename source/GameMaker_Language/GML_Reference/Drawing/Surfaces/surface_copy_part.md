# surface_copy_part

This function simply takes the image from one surface and copies it onto
another one at the specified local position within that surface (where
the (0,0) position is the top left corner of the destination surface).
You can specify a local x and y position to copy from as well as the
width and height of the section. Please note that these are coordinates
based on the *surface size* and not on the position at which the surface
is being drawn in the room. If the destination surface already has
information this will be overwritten by the copy, and the function does
*not* change the source surface in any way. **NOTE** : When working with
surfaces there is the possibility that they can cease to exist at any
time due to them being stored in texture memory. You should **ALWAYS**
check that a surface exists using [ surface_exists()
](surface_exists) before referencing them directly.

#### Syntax:

``` gml
surface_copy_part(destination, x, y, source, xs, ys, ws, hs);
```

|             |                                                                                                     |                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Argument    | Type                                                                                                | Description                                                |
| destination |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of the surface to copy the other surface to.        |
| x           |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The x position to copy to.                                 |
| y           |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The y position to copy to.                                 |
| source      |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of the surface to be copied.                        |
| xs          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The x position in the source surface to copy from.         |
| ys          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The y position in the source surface to copy from.         |
| ws          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The width of the area in the source surface to copy from.  |
| hs          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The height of the area in the source surface to copy from. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if view_current == 0
{
    surface_copy_part(surf, 0, 0, temp_surf, 0, 0, view_xview[1] - mouse_x, view_yview[1] - mouse_y);
}
else
{
    draw_surface(surf, 0, 0);
}
```

The above code will check the current view being drawn and if it is
view\[0\] it copies the surface indexed in the variable "temp_surf" onto
the surface indexed in the variable "surf". The area copied corresponds
to a rectangle formed by the relative position of the mouse within the
surface as it would be drawn in view\[1\]. If the current view is
anything other than view\[0\] the surface "surf" is drawn to the screen.
