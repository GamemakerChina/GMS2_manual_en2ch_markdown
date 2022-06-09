# draw_vertex_texture_colour

This function defines the position of a textured vertex for a primitive.
The final look of the primitive will depend on the primitive type chosen
to draw (See [ draw_primitive_begin() ](draw_primitive_begin) for
more information), the order with which you add the vertices to it, the
position of the start and end points that you give for the texture
sample and the colour and alpha values that you have set. To maintain
the texture appearance while changing only the alpha, a value of -1 (or
c_white ) may be used for the colour argument. To end and draw the
primitive you must call [ draw_primitive_end() ](draw_primitive_end)
. ** NOTE ** For a texture to repeat it must be a power of two in size,
ie: 32x32, 128x128, etc...

#### Syntax:

``` gml
draw_vertex_texture_colour(x, y, xtex, ytex, col, alpha)
```

|          |                                                                                                           |                                                                                        |
|----------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Argument | Type                                                                                                      | Description                                                                            |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x coordinate of the vertex.                                                        |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y coordinate of the vertex.                                                        |
| xtex     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x coordinate within the texture.                                                   |
| ytex     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y coordinate within the texture.                                                   |
| col      |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour to blend with the texture at this vertex (-1 or c_white for no blending).   |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The alpha to draw this vertex with (0-1).                                              |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_colour(c_white); var tex = sprite_get_texture(spr_Background, 0); draw_primitive_begin_texture(pr_trianglestrip, tex); draw_vertex_texture_colour(0, 0, 0, 0, c_fuchsia, 1); draw_vertex_texture_colour(640, 0, 1, 0, c_yellow,
1); draw_vertex_texture_colour(0, 480, 0, 1, c_aqua, 1); draw_vertex_texture_colour(640, 480, 1, 1, c_lime, 1); draw_primitive_end();
```

The above code will draw a 4 vertex triangle strip (making a rectangle)
textured with the texture held in the "tex" variable, and the whole
texture will be used to cover the completed primitive, and it will be
blended with four different colours.
