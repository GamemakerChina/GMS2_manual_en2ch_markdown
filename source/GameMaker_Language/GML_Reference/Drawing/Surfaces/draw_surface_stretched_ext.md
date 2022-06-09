# draw_surface_stretched_ext

This function does exactly the same as the [ draw_surface_stretched()
](draw_surface_stretched) function with the added ability to set the
colour blending and alpha value for the surface when it is drawn
(similar to the function [ draw_surface_ext() ](draw_surface_ext) ).
NOTE When working with surfaces there is the possibility that they can
cease to exist at any time due to them being stored in texture memory.
You should **ALWAYS** check that a surface exists using [
surface_exists() ](surface_exists) before referencing them directly.
TIP How a surface appears depends on its contents, especially the alpha
values inside the surface. A surface
[cleared](../Colour_And_Alpha/draw_clear_alpha) with an alpha of 0
may appear different from a surface cleared with an alpha of 1, due to
the way they blend with the background. Take care of this whenever you
notice a difference in the way something renders on a custom surface as
opposed to the [application_surface](application_surface) .

#### Syntax:

``` gml
draw_surface_stretched_ext(id, x, y, w, h, col, alpha);
```

|          |                                                                                                           |                                              |
|----------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                      | Description                                  |
| id       |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)        | The unique ID value of the surface to draw.  |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x position of where to draw the surface. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y position of where to draw the surface. |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The width at which to draw the surface.      |
| h        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The height at which to draw the surface.     |
| colour   |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour with which to colour the surface. |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The alpha with which to blend the surface.   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_surface_stretched_ext(surf, x, y, 200, 200, c_white, 0.5);
```

This will draw the given surface with its left corner at the instances
x/y position and it will be stretched to occupy an area of 200x200
pixels with no blending, but partial transparency.
