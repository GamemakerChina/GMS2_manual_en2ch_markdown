# view_set_surface_id

With this variable you can set the contents of a view port to draw to a
surface. When working with surfaces, it is often required to capture the
*whole* visible region of the screen to the surface, and so you would
assign it to a view port using this function. This means that everything
that is shown in the chosen view port will now be drawn to the assigned
surface and the contents of that view port will no longer be displayed,
meaning that you will need to either:

-   Enable a new view and draw the surface only in that view (using [
    view_current ](view_current) to check which view is being drawn)
-   Draw the surface in the Draw GUI or Post Draw event of an instance,
    since these events are independent of views.

When using this function you give the view port index (from 0 to 7) and
a surface index (either the [ application_surface
](../../Drawing/Surfaces/application_surface) or the unique index
value returned by the function [ surface_create()
](../../Drawing/Surfaces/surface_create) ) or, if a surface has
previously been assigned and you want to remove it, a value of -1. For
more examples on setting the view port to a surface see the variable [
view_surface_id ](view_surface_id) . IMPORTANT Care must be taken
when drawing surfaces or textures to a view with a surface assigned to
it, because if you try to draw the view's assigned surface (or its
texture) inside that same view, you will get an error as you are
essentially trying to draw a texture onto itself.

#### Syntax:

``` gml
view_set_surface_id(view_port, surf)
```

|           |                                                                                                     |                                  |
|-----------|-----------------------------------------------------------------------------------------------------|----------------------------------|
| Argument  | Type                                                                                                | Description                      |
| view_port |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The view port to target (0 - 7)  |
| surf      |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The surface to apply to the view |

#### Returns:

``` gml
 Real
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
