# surface_resize

This function will resize a surface to the given dimensions (in pixels).
The "surface_id" is that of a surface you have created previously, or
the [ application_suface ](application_surface) , and the function
will resize that surface. Note that this will neither crop nor stretch
the contents of the surface, but rather it destroys the current surface
and recreates it with the same handle (surface_id) with the new
dimensions, meaning that it will need to be cleared and drawn to again
(unless it is the application_surface in which case GameMaker will do
this automatically). **NOTE** : If you are resizing the application
surface, these changes will not be registered until the start of the
next draw frame, meaning that calling the [ surface_get_width()
](surface_get_width) or [ surface_get_height()
](surface_get_height) functions in the same event or step will
return the previous values.

#### Syntax:

``` gml
surface_resize(surface_id, w, h);
```

|            |                                                                                                     |                                  |
|------------|-----------------------------------------------------------------------------------------------------|----------------------------------|
| Argument   | Type                                                                                                | Description                      |
| surface_id |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of the surface to change. |
| w          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The width of the new surface.    |
| h          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The height of the new surface.   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if view_wport[0] != surface_get_width(application_surface) || view_hport[0] != surface_get_height(application_surface)
{
    surface_resize(application_surface, view_wport[0],view_hport[0]);
}
```

The above code will check the view port size against that of the surface
"aplication_surface" and if it is different, the surface is re-sized.
