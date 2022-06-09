# draw_surface_part

With this function you can draw part of any surface at a given position
within the room. As with [draw_surface()](draw_surface) you can
specify a surface, but you then need to specify the *relative
coordinates* within the surface of an area to select for drawing. This
means that a left position of 0 and a top position of 0 would be the top
left corner of the surface and all further coordinates should be taken
from that position. NOTE When working with surfaces there is the
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
draw_surface_part(id, left, top, w, h, x, y);
```

|          |                                                                                                     |                                                           |
|----------|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                                                | Description                                               |
| id       |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The unique ID value of the surface to draw.               |
| left     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The left position in the surface of the part to be drawn. |
| top      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The top position in the surface of the part to be drawn.  |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The width of the part to be draw, from left.              |
| h        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The height of the part to be drawn, from top.             |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The x position of where to draw the surface.              |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The y position of where to draw the surface.              |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_surface_part(surf, 8, 8, 32, 32, x, y);
```

This will draw a 32x32 area 8px by 8px in from the top left of the
surface indexed in "surf", at the instances (x,y) position.
