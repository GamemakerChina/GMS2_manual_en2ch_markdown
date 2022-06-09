# surface_save

This function will save a surface to disc using the given filename. The
surface *must* be saved as a \*.png format file.

#### Syntax:

``` gml
surface_save(surface_id, fname);
```

|            |                                                                                                     |                                                     |
|------------|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument   | Type                                                                                                | Description                                         |
| surface_id |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of the surface to set as the drawing target. |
| fname      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                            | The name of the saved image file.                   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check_pressed(ord("S")
{
    surface_save(surf, "test.png");
}
```

The above code will check to see if the user presses the "S" key on the
keyboard and if they do it will save the surface indexed in the variable
"surf" to disc.
