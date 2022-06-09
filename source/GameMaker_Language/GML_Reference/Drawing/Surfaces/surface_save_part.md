# surface_save_part

This function will save a part of a surface to disc using the given
filename. The surface *must* be saved as a \*.png format file, and the
(x,y) position must be given as local coordinates to the surface,
bearing in mind that the top left corner of the surface is always (0,0).

#### Syntax:

``` gml
surface_save_part(surface_id, fname, x, y, width, height);
```

|            |                                                                                                     |                                                     |
|------------|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument   | Type                                                                                                | Description                                         |
| surface_id |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of the surface to set as the drawing target. |
| fname      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                            | The name of the saved image file.                   |
| x          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The starting x position within the surface.         |
| y          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The starting y position within the surface.         |
| width      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The width of the part to save.                      |
| height     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The height of the part to save.                     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check_pressed(ord("S")
{
    surface_save_part(surf, "test.png", 0, 0, 100, 100);
}
```

The above code will check to see if the user presses the "S" key on the
keyboard and if they do it will save a part of the surface indexed in
the variable "surf" to disc.
