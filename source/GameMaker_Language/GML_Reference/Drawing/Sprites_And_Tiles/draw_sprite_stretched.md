# draw_sprite_stretched

This function simply takes a sprite resource and stretches it over the
given width and height so that it occupies that area. As with [
draw_sprite() ](draw_sprite) you can specify a sprite and a
sub-image for drawing, then the x / y position in the room for the
sprite to be drawn at and finally a width and a height (which must be
pixel values). The image below shows the result of this function with
different sets of arguments:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/spr_stretch.png)  
NOTE When drawing with this function, the sprite [x
offset](../../Asset_Management/Sprites/Sprite_Instance_Variables/sprite_xoffset)
and [y
offset](../../Asset_Management/Sprites/Sprite_Instance_Variables/sprite_yoffset)
(or origins) are ignored and the sprite is drawn with the top-left
corner at the specified x/y position in the room. If used with a Nine
Slice enabled sprite, it will retain any detail after scaling depending
on your Nine Slice settings in the [Sprite
Editor](../../../../The_Asset_Editors/Sprites) . See the page on
[Nine
Slice](../../../../The_Asset_Editors/Sprite_Properties/Nine_Slices)
for more information.

#### Syntax:

``` gml
draw_sprite_stretched(sprite, subimg, x, y, w, h);
```

|          |                                                                         |                                                                                                                         |
|----------|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                                                                             |
| sprite   |  [Sprite Asset](../../../../../The_Asset_Editors/Sprites)           | The index of the sprite to draw.                                                                                        |
| subimg   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The subimg (frame) of the sprite to draw (image_index or -1 correlate to the current frame of animation in the object). |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of where to draw the sprite.                                                                           |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of where to draw the sprite.                                                                           |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The width of the area the stretched sprite will occupy.                                                                 |
| h        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The height of the area the stretched sprite will occupy.                                                                |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_sprite_stretched(sprite_index, image_index, x, y, sprite_width, sprite_height / 2);
```

This will draw the instance's assigned sprite and its sub-image with the
left corner at the instance x/y position. Its width is set to the same
as the sprite, and the height is the sprite height divided by two.
