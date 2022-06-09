# draw_texture_flush

With this function you can remove all textures from video memory, and
they will then be reloaded on first use. This is the only effective way
to manage video memory when you have multiple texture pages for a game,
and you should flush the texture memory between levels on your game and
organise the graphics using the texture group feature to ensure that the
minimum number of textures are used. It is worth noting that *by
default* on all targets, texture pages will only be loaded as they are
required and you can use the various prefetch and flush functions for
sprites (found
[here](../../Asset_Management/Sprites/Sprite_Manipulation/Sprite_Manipulation)
) to manage things as well as this function.

#### Syntax:

``` gml
draw_texture_flush();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_texture_flush();
```

The above code flushes the video memory of texture data, and would
probably be placed in the create event of the first instance of an
object placed in the room.
