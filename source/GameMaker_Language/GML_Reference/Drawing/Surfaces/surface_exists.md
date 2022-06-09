# surface_exists

This function is essential when working with surfaces due to their
volatile nature. Surfaces are always held in texture memory which means
that they can be destroyed from one moment to the next (for example,
when a screensaver starts on windows, or when minimised on an Android
device), so you should always check that a surface exists before doing
anything with it (this includes drawing it to the screen). The example
code below shows a typical use of this command in the draw event of an
instance to check for a surface and re-create it if it has been removed
(note that the surface will have been originally created in the create
event of the object).

#### Syntax:

``` gml
surface_exists(surface_id);
```

|            |                                                                                                     |                                 |
|------------|-----------------------------------------------------------------------------------------------------|---------------------------------|
| Argument   | Type                                                                                                | Description                     |
| surface_id |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of the surface to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !surface_exists(surf)
{
    surf = surface_create(1024, 1024);
}
else
{
    if view_current = 1
    {
        draw_surface(surf,0,0);
    }
}
```

The above code will check to see if a surface indexed in the variable
"surf" exists, and if it does not, it will re-create it. If it does
exist, it then checks to see which view is currently being drawn and if
it is view\[1\] it draws the surface.
