# draw_surface_part_ext

This function will draw a part of the chosen surface at the given
position following the same rules as per [ draw_surface_part()
](draw_surface_part) , only now you can scale the part, blend a
colour with it, or change its alpha when drawing it to the screen (the
same as when drawing a surface with [ draw_surface_ext()
](draw_surface_ext) ). NOTE When working with surfaces there is the
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
draw_surface_part_ext(id, left, top, w, h, x, y, xscale, yscale, colour, alpha);
```

|          |                                                                                                           |                                                           |
|----------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                                                      | Description                                               |
| id       |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)        | The unique ID value of the surface to draw.               |
| left     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The left position in the surface of the part to be drawn. |
| top      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The top position in the surface of the part to be drawn.  |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The width of the part to be draw, from left.              |
| h        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The height of the part to be drawn, from top.             |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x position of where to draw the surface.              |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y position of where to draw the surface.              |
| xscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The horizontal scaling the part should be drawn with.     |
| yscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The vertical scaling the part should be drawn with.       |
| colour   |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour blending the part should be drawn with.        |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The alpha transparency the part should be drawn with.     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_surface_part_ext(surf, 8, 8, 32, 32, x, y, 2, 0.5, c_black, 1);
```

This will draw a 32x32 pixel area from 8x8 pixels into the surface
indexed in the variable "surf". It will be stretched to double its usual
width but half its usual height. It will be opaque and it will be
blended with black (turning it into a silhouette).
