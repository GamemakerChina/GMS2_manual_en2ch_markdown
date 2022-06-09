# surface_create

This function is used to create a surface and will return the index of
the surface which should be stored in a variable for future function
calls. When the surface is first created, it may contain "noise" as
basically it is just an area of memory that is put aside for the purpose
(and that memory may still contain information), so you may want to
clear the surface before use with a function like [ draw_clear_alpha()
](../Colour_And_Alpha/draw_clear_alpha) . It is highly recommended
that all surfaces be created with a size that is a power of 2, ie: 16,
128, 512 or 1024 pixels in size, for example. This is not exactly
necessary on certain platforms (like Windows and MacOS) but it will
certainly increase compatibility on those targets, while for HTML5 and
devices it is essential and very it's important that you remember this
or you may run into problems later.

#### Syntax:

``` gml
surface_create(w, h);
```

|          |                                                                         |                                          |
|----------|-------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                    | Description                              |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The width of the surface to be created.  |
| h        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The height of the surface to be created. |

#### Returns:

``` gml
 Surface ID
```

#### Example:

``` gml
if !surface_exists(surf)
{
    surf = surface_create(1024, 1024);
    surface_set_target(surf);
    draw_clear_alpha(c_black, 0);
    surface_reset_target();
    view_surface_id[0] = surf;
}
```

The above code checks to see if a surface exists and if it does not it
will create a surface that is 1024 pixels wide and 1024 pixels high,
assigning the index to the variable "surf". The drawing target is then
set to the new surface, which is cleared and made transparent before
having the drawing target reset to the display. Finally the surface is
assigned to a view.
