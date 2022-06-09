# draw_sprite_general

This function combines the function [ draw_sprite_ext()
](draw_sprite_ext) with the function [ draw_sprite_part()
](draw_sprite_part) , adding in some additional blending options so
that each corner of the final sprite part can be blended with an
individual colour. **NOTE** : Colour blending is only recommended for
the HTML5 target when WebGL is enabled, although you can still set the
blending colour if it is not enabled and it will blend the sprite as
normal. However all blending in this way creates a duplicate sprite
which is then stored in the cache and used when required. This is far
from optimal and if you use multiple colour changes it will slow down
your games performance unless you activate WebGL. if you do not wish to
use WebGL, then you can set the font cache size to try and limit this
should it be necessary using the function [ sprite_set_cache_size()
](../../Asset_Management/Sprites/Sprite_Manipulation/sprite_set_cache_size_ext)
. **NOTE** : This function may not work as expected when using skeleton
animation sprites, and you may find that the function only draws the
first frame of the default pose. You should be using the
draw_skeleton\_\* functions instead.

#### Syntax:

``` gml
draw_sprite_general(sprite, subimg, left, top, width, height, x, y, xscale, yscale, rot, c1, c2, c3, c4, alpha);
```

|          |                                                                                                           |                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                      | Description                                                                                                             |
| sprite   |  [Sprite Asset](../../../../../The_Asset_Editors/Sprites)                                             | The index of the sprite to draw.                                                                                        |
| subimg   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The subimg (frame) of the sprite to draw (image_index or -1 correlate to the current frame of animation in the object). |
| left     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x position on the sprite of the top left corner of the area to draw.                                                |
| top      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y position on the sprite of the top left corner of the area to draw.                                                |
| width    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The width of the area to draw.                                                                                          |
| height   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The height of the area to draw.                                                                                         |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x coordinate of where to draw the sprite.                                                                           |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y coordinate of where to draw the sprite.                                                                           |
| xscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The horizontal scaling of the sprite, as a multiplier: 1 = normal scaling, 0.5 is half etc...                           |
| yscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The vertical scaling of the sprite, as a multiplier: 1 = normal scaling, 0.5 is half etc...                             |
| rot      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The rotation of the sprite. 0=normal, 90=turned 90 degrees counter-clockwise etc.                                       |
| c1       |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour with which to blend the top left area of the sprite.                                                         |
| c2       |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour with which to blend the top right area of the sprite.                                                        |
| c3       |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour with which to blend the bottom right area of the sprite.                                                     |
| c4       |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour with which to blend the bottom left area of the sprite.                                                      |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The alpha of the sprite (from 0 to 1 where 0 is transparent and 1 opaque).                                              |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_sprite_general(sprite_index, image_index, 8, 8, sprite_width-16, sprite_height-16, x, y, 2, 0.5, 180, c_white, c_white, c_black, c_black, 1);
```

This will draw the instances assigned sprite (sprite_index) and its
current frame of animation (image_index), however it will shave an 8px
margin off all four sides of the sprite. It will be stretched to double
its usual width but half its usual height. It will be opaque, and upside
down. The top area of the sprite will be blended white and hence normal,
but the bottom area will be black, meaning the sprite will go from
normal to a silhouette downwards in a smooth gradient.
