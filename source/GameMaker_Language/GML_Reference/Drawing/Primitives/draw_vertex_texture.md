# draw_vertex_texture

This function defines the position of a textured vertex for a primitive.
The final look of the primitive will depend on the primitive type chosen
to draw (See [ draw_primitive_begin() ](draw_primitive_begin) for
more information), the order with which you add the vertexes to it and
the position of the start point you set for the texture. To end and draw
the primitive you must call [ draw_primitive_end()
](draw_primitive_end) . You can also choose to draw only *part* of
the texture over the surface of the primitive by setting the appropriate
xtex/ytex position to sample to (these coordinates are also known as the
**UV** points). This point is defined by a value between 0 and 1 with
the top left corner of the image to use being the (0,0) point and the
bottom right corner being the (1,1) point. In this way you can texture a
primitive with only a part of the source image asset. When drawing a
textured primitive, the texture will be blended with the colour set by
draw_set_colour . This means that to draw the texture with no blending
this should be set to c_white , as shown in the example below. ** NOTE
** For a texture to repeat it must be a power of two in size, ie: 32x32,
128x128, etc...

#### Syntax:

``` gml
 draw_vertex_texture(x, y, xtex, ytex)
```

|          |                                                                         |                                          |
|----------|-------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                    | Description                              |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the vertex.          |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the vertex.          |
| xtex     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The width of the texture sample to use.  |
| ytex     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The height of the texture sample to use. |

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
