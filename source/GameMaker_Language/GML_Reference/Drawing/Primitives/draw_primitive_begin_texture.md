# draw_primitive_begin_texture

This function must be called before you define the vertices of a
textured primitive. You must give the kind of primitive to use (see [
draw_primitive_begin() ](draw_primitive_begin) for more information)
and the **id** of a texture to use, which can be a sprite or background
image asset. This asset **id** can be gotten from the functions [
sprite_get_texture()
](../../Asset_Management/Sprites/Sprite_Information/sprite_get_texture)
, for example (use -1 for no texture). ** NOTE ** For a texture to
repeat it must be a power of two in size, ie: 32x32, 128x128, etc...

#### Syntax:

``` gml
draw_primitive_begin_texture(kind, tex)
```

|          |                                                                                                                                 |                                              |
|----------|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                                            | Description                                  |
| kind     |  [Primitive Type Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/draw_primitive_begin)         | The kind of primitive you are going to draw. |
| tex      |  [Texture](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Information/sprite_get_texture)  | The texture to use with the primitive.       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_colour(c_white);
var tex = sprite_get_texture(spr_Background, 0);
draw_primitive_begin_texture(pr_trianglestrip, tex);
draw_vertex_texture(0, 0, 0, 0);
draw_vertex_texture(640, 0, 1, 0);
draw_vertex_texture(0, 480, 0, 1);
draw_vertex_texture(640, 480, 1, 1);
draw_primitive_end();
```

The above code will draw a 4 vertex triangle strip (making a rectangle)
textured with the texture held in the "tex" variable, and the whole
texture will be used to cover the completed primitive.
