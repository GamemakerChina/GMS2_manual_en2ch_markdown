# tileset_get_texture

This function returns a special *pointer* for the tile set texture page.
This value can then be used in other draw functions, particularly in the
[2D
primitive](../../Drawing/Primitives/Primitives_And_Vertex_Formats)
functions, as well as the [Shader](../Shaders/Shaders) functions.
You can get more information about the returned texture page using the
different texture\_ functions found
[here](../../Drawing/Textures/Textures) . NOTE On HTML5, this
returns a struct instead of a texture pointer, as a pointer cannot be
used on that platform. However this does not change the use of the
returned value, as its usage in [texture
functions](../../Drawing/Textures/Textures) still remains the same.

#### Syntax:

``` gml
tileset_get_texture(tileset);
```

|          |                                                                    |                                   |
|----------|--------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                               | Description                       |
| tileset  |  [Tile Set Asset](../../../../../The_Asset_Editors/Tile_Sets)  | The index of the tile set to use. |

#### Returns

``` gml
 Texture
```

#### Example:

``` gml
var tex;
tex = tileset_get_texture(spr_Wall, 0);
draw_primitive_begin_texture(pr_trianglestrip, tex);
draw_vertex_texture(0, 0, 0, 0);
draw_vertex_texture(480, 0, 1, 0);
draw_vertex_texture(480, 640, 1, 1);
draw_vertex_texture(0, 640, 0, 1);
draw_primitive_end();
```

The above code will draw a 4 vertex triangle strip textured with the
texture held in the "tex" variable.
