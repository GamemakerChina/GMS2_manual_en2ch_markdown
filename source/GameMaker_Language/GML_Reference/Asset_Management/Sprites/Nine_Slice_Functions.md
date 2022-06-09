# Nine Slice Functions

In addition to the Nine Slice section in the [Sprite
Editor](../../../../The_Asset_Editors/Sprites) , GameMaker provides
functions for setting Nine Slice properties for sprites at runtime.
Before reading about these functions, it is recommended to read [this
page](../../../../The_Asset_Editors/Sprite_Properties/Nine_Slices)
to get an understanding of the Nine Slice technique. The
following functions can be used to retrieve and change Nine Slice
properties for a sprite asset at runtime:

-   [sprite_nineslice_create](Sprite_Manipulation/sprite_nineslice_create)
-   [sprite_get_nineslice](Sprite_Information/sprite_get_nineslice)
-   [sprite_set_nineslice](Sprite_Manipulation/sprite_set_nineslice)

These functions make use of a Nine Slice struct, and you can read about
the contents of that struct on [this page](Nine_Slice_Struct) .

## Drawing Nine Slice Sprites

There are no separate functions for drawing Nine Slice sprites as they
work with the existing sprite drawing functions (except for functions
that draw only a part of the sprite or distort it, such as
[draw_sprite_part()](../../Drawing/Sprites_And_Tiles/draw_sprite_part)
or
[draw_sprite_pos()](../../Drawing/Sprites_And_Tiles/draw_sprite_pos)
). It is recommended to use the [ draw_sprite_stretched()
](../../Drawing/Sprites_And_Tiles/draw_sprite_stretched) function to
draw a Nine Slice sprite, as it allows you to specify the absolute
dimensions of the sprite in pixels and will be easy to use along with
Nine Slice. You can also use [ draw_sprite_ext()
](../../Drawing/Sprites_And_Tiles/draw_sprite_ext) which instead
takes scale values.
