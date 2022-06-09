# draw_sprite_part_ext

This function will draw a part of the chosen sprite at the given
position following the same rules as per [ draw_sprite_part()
](draw_sprite_part) , only now you can scale the part, blend a
colour with it, or change its alpha when drawing it to the screen (the
same as when drawing a sprite with [ draw_sprite_ext()
](draw_sprite_ext) ). You should note that if the texture page
permits automatic cropping then this function may not work as expected,
since the extra "empty" space around the sprite will have been removed
for creating the texture page. To resolve this issue, you will need to
set the texture page settings (in the [Texture Group
Editor](../../../../Settings/Texture_Groups) ) to disable the
**Automatic Crop** . ** NOTE ** When drawing with this function, the
sprite [x
offset](../../Asset_Management/Sprites/Sprite_Instance_Variables/sprite_xoffset)
and [y
offset](../../Asset_Management/Sprites/Sprite_Instance_Variables/sprite_yoffset)
are ignored and the sprite part will be drawn with the top left corner
at the specified x / y position in the room. **NOTE** : This function is
only useful for **bitmap** sprites and will not work with SWF or JSON
(Spine) sprites. **NOTE** : Colour blending is only recommended for the
HTML5 target when WebGL is enabled, although you can still set the
blending colour if it is not enabled and it will blend the sprite as
normal. However all blending in this way creates a duplicate sprite
which is then stored in the cache and used when required. This is far
from optimal and if you use multiple colour changes it will slow down
your games performance unless you activate WebGL. if you do not wish to
use WebGL, then you can set the font cache size to try and limit this
should it be necessary using the function [ sprite_set_cache_size()
](../../Asset_Management/Sprites/Sprite_Manipulation/sprite_set_cache_size_ext)
.

#### Syntax:

``` gml
draw_sprite_part_ext(sprite, subimg, left, top, width, height, x, y, xscale, yscale, colour, alpha);
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
| colour   |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour with which to blend the sprite. c_white is to display it normally.                                           |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The alpha of the sprite (from 0 to 1 where 0 is transparent and 1 opaque).                                              |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_sprite_part_ext(sprite_index, image_index, 8, 8, sprite_width-16, sprite_height-16, x, y, 2, 0.5, c_black, 1);
```

This will draw the instances assigned sprite (sprite_index) and its
current frame of animation (image_index), however it will shave an 8px
margin off all four sides of the sprite. It will then be stretched to
double its usual width but half its usual height, and although the alpha
is still 1, it will be blended with black (turning it into a
silhouette).
