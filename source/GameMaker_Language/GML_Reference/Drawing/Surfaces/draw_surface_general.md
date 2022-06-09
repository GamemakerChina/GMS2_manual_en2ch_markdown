# draw_surface_general

This function combines the function [ draw_surface_ext()
](draw_surface_ext) with the function [ draw_surface_part()
](draw_surface_part) , adding in some additional blending options so
that each corner of the final surface part can be blended with an
individual colour. ** NOTE ** Gradient blending is not available for the
HTML5 target unless WebGL is enabled. NOTE When working with surfaces
there is the possibility that they can cease to exist at any time due to
them being stored in texture memory. You should **ALWAYS** check that a
surface exists using [ surface_exists() ](surface_exists) before
referencing them directly. TIP How a surface appears depends on its
contents, especially the alpha values inside the surface. A surface
[cleared](../Colour_And_Alpha/draw_clear_alpha) with an alpha of 0
may appear different from a surface cleared with an alpha of 1, due to
the way they blend with the background. Take care of this whenever you
notice a difference in the way something renders on a custom surface as
opposed to the [application_surface](application_surface) .

#### Syntax:

``` gml
draw_surface_general(id, left, top, w, h, x, y, xscale, yscale, rot, c1, c2, c3, c4, alpha);
```

|          |                                                                                                           |                                                           |
|----------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                                                      | Description                                               |
| id       |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)        | The unique ID value of the surface to draw.               |
| left     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The left position in the surface of the part to be drawn. |
| top      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The top position in the surface of the part to be drawn.  |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The width of the part to be draw, from left.              |
| h        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The height of the part to be draw, from top.              |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x position of where to draw the surface.              |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y position of where to draw the surface.              |
| xscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The horizontal scaling to draw the surface with.          |
| yscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The vertical scaling to draw the surface with.            |
| rot      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The rotation or angle to draw the surface with.           |
| c1       |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour of the top left corner of the surface.         |
| c2       |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour of the top right corner of the surface.        |
| c3       |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour of the bottom right corner of the surface.     |
| c4       |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour of the bottom left corner of the surface.      |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The alpha transparency to draw the surface with..         |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_surface_general(surf, 8, 8, 32, 32, x, y, 2, 0.5, 180, c_white, c_white, c_black, c_black, 1);
```

This will draw a 32x32 pixel area from 8x8 pixels into the surface. It
will be stretched to double its usual width but half its usual height.
It will be opaque, and upside down. The top area of the surface will be
blended white and hence normal, but the bottom area will be black,
meaning the surface will go from normal to silhouette downwards in a
smooth gradient.
