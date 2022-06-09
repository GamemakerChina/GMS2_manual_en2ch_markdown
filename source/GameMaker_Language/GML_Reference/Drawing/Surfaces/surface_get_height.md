# surface_get_height

This function simply returns the height, in pixels, of the indexed
surface. It should be noted that if you call this to check the
application_surface immediately after having changed its size using [
surface_resize() ](surface_resize) it will not return the new value
as the change needs a step or two to be fully processed. After waiting a
step it should return the new size correctly. **NOTE** : When working
with surfaces there is the possibility that they can cease to exist at
any time due to them being stored in texture memory. You should
**ALWAYS** check that a surface exists using [ surface_exists()
](surface_exists) before referencing them directly.

#### Syntax:

``` gml
surface_get_height(surface_id);
```

|            |                                                                                                     |                                             |
|------------|-----------------------------------------------------------------------------------------------------|---------------------------------------------|
| Argument   | Type                                                                                                | Description                                 |
| surface_id |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of the surface to get the height of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
sh = surface_get_height(surf);
```

The above code will store the height of the surface indexed in the
variable "surf" in the variable "sh".
