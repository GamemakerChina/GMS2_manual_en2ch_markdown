# draw_primitive_end

This function must be called when you have finished defining the points
of your primitive. If you do not call this function, *nothing will be
drawn* as this effectively tells GameMaker that you have finished and
that it can now draw the defined primitive.

#### Syntax:

``` gml
draw_primitive_end()
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_colour(c_white); var tex = sprite_get_texture(spr_Background, 0); draw_primitive_begin_texture(pr_trianglestrip, tex); draw_vertex_texture(0, 0, 0, 0); draw_vertex_texture(640, 0, 1, 0); draw_vertex_texture(0, 480,
0, 1); draw_vertex_texture(640, 480, 1, 1); draw_primitive_end();
```

The above code will draw a 4 vertex triangle strip textured with the
texture held in the "tex" variable.
