# draw_surface_ext

This function will draw the given surface as in the function [
draw_surface() ](draw_surface) but with additional options to change
the scale, blending, rotation and alpha of the surface being drawn.
Changing these values does *not* modify the resource in any way (only
how it is drawn). NOTE When working with surfaces there is the
possibility that they can cease to exist at any time due to them being
stored in texture memory. You should **ALWAYS** check that a surface
exists using [ surface_exists() ](surface_exists) before referencing
them directly. TIP How a surface appears depends on its contents,
especially the alpha values inside the surface. A surface
[cleared](../Colour_And_Alpha/draw_clear_alpha) with an alpha of 0
may appear different from a surface cleared with an alpha of 1, due to
the way they blend with the background. Take care of this whenever you
notice a difference in the way something renders on a custom surface as
opposed to the [application_surface](application_surface) .

#### Syntax:

``` gml
draw_surface_ext(id, x, y, xscale, yscale, rot, col, alpha);
```

|          |                                                                                                           |                                                 |
|----------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Argument | Type                                                                                                      | Description                                     |
| id       |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)        | The unique ID value of the surface to draw.     |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x position of where to draw the surface.    |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y position of where to draw the surface.    |
| xscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The horizontal scale.                           |
| yscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The vertical scale.                             |
| rot      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The rotation or angle to draw the surface.      |
| col      |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour with which to blend the surface.     |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The alpha transparency for drawing the surface. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_surface_ext(surf, 0, 0, 2, 2, 0, c_red, 0.5);
```

The above code will draw a the surface indexed in the variable "surf" at
the (0,0) position in the room, with twice the original scale, blended
red and semi transparent.
