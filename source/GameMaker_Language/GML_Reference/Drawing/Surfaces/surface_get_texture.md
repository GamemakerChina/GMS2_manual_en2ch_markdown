# surface_get_texture

This function returns a special *pointer* for the surface's texture.
This value can then be used in other draw functions, particularly in
general 3D and some of the 2D primitive functions. NOTE When working
with surfaces there is the possibility that they can cease to exist at
any time due to them being stored in texture memory. You should
**ALWAYS** check that a surface exists using [ surface_exists()
](surface_exists) before referencing them directly. NOTE On HTML5,
this returns a struct instead of a texture pointer, as a pointer cannot
be used on that platform. However this does not change the use of the
returned value, as its usage in [texture
functions](../Textures/Textures) still remains the same.

#### Syntax:

``` gml
surface_get_texture(surface_id);
```

|            |                                                                                                     |                                            |
|------------|-----------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument   | Type                                                                                                | Description                                |
| surface_id |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of the surface to get the width of. |

#### Returns:

``` gml
 Texture
```

#### Example:

``` gml
var tex;
tex = surface_get_texture(surf);
draw_primitive_begin_texture(pr_trianglestrip, tex);
draw_vertex_texture(0, 480, 0, 0);
draw_vertex_texture(640, 480, 1, 0);
draw_vertex_texture(640, 480, 1, 1);
draw_vertex_texture(0, 480, 0, 1);
draw_primitive_end();
```

The above code will draw a 4 vertex triangle strip textured with the
texture held in the "tex" variable, which is itself taken from a
previously created surface.
