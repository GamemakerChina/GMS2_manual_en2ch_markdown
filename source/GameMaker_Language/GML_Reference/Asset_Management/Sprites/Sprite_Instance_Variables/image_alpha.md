# image_alpha

This variable is used to get or to set the alpha value for the sprite.
Alpha is always calculated as a value between 0 and 1 where 0 is
completely transparent and 1 is completely opaque. Please note that for
changes in this variable to be visible, the instance should have either
*no* draw event (and so GameMaker will default draw the sprite) or be
drawn using one of the extended drawing functions like [
](https://docs2.yoyogames.com/source/_build/3_scripting/4_gml_reference/drawing/sprites_and_tiles/draw_selfl)
[ draw_self() ](../../../Drawing/Sprites_And_Tiles/draw_self) [
](https://docs2.yoyogames.com/source/_build/3_scripting/4_gml_reference/drawing/sprites_and_tiles/draw_selfl)
or [ draw_sprite_ext()
](../../../Drawing/Sprites_And_Tiles/draw_sprite_ext) .

#### Syntax:

``` gml
image_alpha;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
image_alpha = clamp(image_alpha - 0.01, 0, 1);
```

The above code will slowly reduce the image_alpha until it reaches 0.
