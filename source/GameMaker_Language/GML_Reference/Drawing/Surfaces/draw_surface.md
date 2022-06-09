# draw_surface

With this function you can draw a surface at a given position within the
room, with the top left corner of the surface being drawn at the
specified x/y position. NOTE When working with surfaces there is the
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
draw_surface(id, x, y);
```

|          |                                                                                                     |                                              |
|----------|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                | Description                                  |
| id       |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The unique ID value of the surface to draw.  |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The x position of where to draw the surface. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The y position of where to draw the surface. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _vx = camera_get_view_x(view_camera[0]);
var _vy = camera_get_view_y(view_camera[0]);
draw_surface(surf, _vx, _vy);
```

The above code draws the surface indexed in "surf" at same position as
camera view\[0\].
