# surface_getpixel

This function can be used to get the colour of a specific pixel from a
surface, using the local coordinates of the surface where (0,0) is the
top left corner. This function should *not* be used very often as it is
extremely slow and may cause a pause in your game. **NOTE** : When
working with surfaces there is the possibility that they can cease to
exist at any time due to them being stored in texture memory. You should
**ALWAYS** check that a surface exists using [ surface_exists()
](surface_exists) before referencing them directly.

#### Syntax:

``` gml
surface_getpixel(surface_id, x, y);
```

|            |                                                                                                     |                                                            |
|------------|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Argument   | Type                                                                                                | Description                                                |
| surface_id |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of the surface.                                     |
| x          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The x position on the surface from which to get the pixel. |
| y          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The y position on the surface from which to get the pixel. |

#### Returns:

``` gml
 Colour
```

#### Example:

``` gml
col = surface_getpixel(surf, 56, 78 );
```

This will return the colour of the pixel at coordinates (56,78) of the
surface indexed in the variable "surf".
