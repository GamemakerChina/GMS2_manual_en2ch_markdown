# draw_sprite_stretched_ext

This function does exactly the same as the [ draw_sprite_stretched()
](draw_sprite_stretched) function with the added ability to set the
colour blending and alpha value for the sprite when it is drawn (similar
to the function [ draw_sprite_ext() ](draw_sprite_ext) ). NOTE When
drawing with this function, the sprite [x
offset](../../Asset_Management/Sprites/Sprite_Instance_Variables/sprite_xoffset)
and [y
offset](../../Asset_Management/Sprites/Sprite_Instance_Variables/sprite_yoffset)
(or origins) are ignored and the sprite is drawn with the top-left
corner at the specified x/y position in the room. NOTE Colour blending
is only recommended for the HTML5 target when WebGL is enabled, although
you can still set the blending colour if it is not enabled and it will
blend the sprite as normal. However all blending in this way creates a
duplicate sprite which is then stored in the cache and used when
required. This is far from optimal and if you use multiple colour
changes it will slow down your games performance unless you activate
WebGL. if you do not wish to use WebGL, then you can set the font cache
size to try and limit this should it be necessary using the function [
sprite_set_cache_sizee()
](../../Asset_Management/Sprites/Sprite_Manipulation/sprite_set_cache_size_ext)
.

#### Syntax:

``` gml
draw_sprite_stretched_ext(sprite, subimg, x, y, w, h, colour, alpha);
```

|          |                                                                                                           |                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                      | Description                                                                                                             |
| sprite   |  [Sprite Asset](../../../../../The_Asset_Editors/Sprites)                                             | The index of the sprite to draw.                                                                                        |
| subimg   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The subimg (frame) of the sprite to draw (image_index or -1 correlate to the current frame of animation in the object). |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x coordinate of where to draw the sprite.                                                                           |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y coordinate of where to draw the sprite.                                                                           |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The width of the area the stretched sprite will occupy.                                                                 |
| h        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The height of the area the stretched sprite will occupy.                                                                |
| colour   |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour with which to blend the sprite. c_white is to display it normally.                                           |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The alpha of the sprite (from 0 to 1 where 0 is transparent and 1 opaque).                                              |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_sprite_stretched_ext(sprite_index, image_index, x, y, sprite_width, sprite_height / 2, c_white, 0.5);
```

This will draw the instances assigned sprite and its sub-image with the
left corner at the instance x /y position. Its width is set to the same
as the sprite, and the height is the sprite height divided by two. It
will also be blended normally but have a partially transparent alpha
value.
