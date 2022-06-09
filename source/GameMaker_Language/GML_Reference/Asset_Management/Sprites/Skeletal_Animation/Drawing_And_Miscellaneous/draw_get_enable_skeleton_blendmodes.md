# draw_get_enable_skeleton_blendmodes

This function returns whether per-slot blend modes for skeletal sprites
are enabled ( true ) or disabled ( false ).

#### Syntax:

``` gml
draw_get_enable_skeleton_blendmodes()
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if (!draw_get_enable_skeleton_blendmodes())
{
    draw_enable_skeleton_blendmodes(true);
}
```

The above code enables per-slot blend modes for skeletal sprites, if
they are disabled.
