# draw_sprite_ext

This function will draw the given sprite as in the function [
draw_sprite() ](draw_sprite) but with additional options to change
the scale, blending, rotation and alpha of the sprite being drawn.
Changing these values does *not* modify the resource in any way (only
how it is drawn), and you can use any of the available [sprite
variables](../../Asset_Management/Sprites/Sprite_Instance_Variables/Sprite_Instance_Variables)
instead of direct values for all the arguments in the function. The
image below illustrates how different values affect the drawing of the
sprite:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/spr_ext.png)  
If used with a Nine Slice enabled sprite, it will retain any
detail after scaling depending on your Nine Slice settings in the
[Sprite Editor](../../../../The_Asset_Editors/Sprites) . See the
page on [Nine
Slice](../../../../The_Asset_Editors/Sprite_Properties/Nine_Slices)
for more information. **NOTE** : Colour blending is only recommended for
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
draw_sprite_ext( sprite, subimg, x, y, xscale, yscale, rot, colour, alpha );
```

|          |                                                                                                           |                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                      | Description                                                                                                             |
| sprite   |  [Sprite Asset](../../../../../The_Asset_Editors/Sprites)                                             | The index of the sprite to draw.                                                                                        |
| subimg   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The subimg (frame) of the sprite to draw (image_index or -1 correlate to the current frame of animation in the object). |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x coordinate of where to draw the sprite.                                                                           |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y coordinate of where to draw the sprite.                                                                           |
| xscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The horizontal scaling of the sprite, as a multiplier: 1 = normal scaling, 0.5 is half etc...                           |
| yscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The vertical scaling of the sprite as a multiplier: 1 = normal scaling, 0.5 is half etc...                              |
| rot      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The rotation of the sprite. 0=right way up, 90=rotated 90 degrees counter-clockwise etc...                              |
| colour   |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour with which to blend the sprite. c_white is to display it normally.                                           |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The alpha of the sprite (from 0 to 1 where 0 is transparent and 1 opaque).                                              |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_sprite_ext(sprite_index, image_index, x, y, image_xscale, image_yscale, image_angle, image_blend, image_alpha);
```

This will draw the instances assigned sprite with all its default values
(essentially the same as using draw_self ).
