# draw_sprite_part

With this function you can draw part of any sprite at a given position
within the room. As with [ draw_sprite() ](draw_sprite) you can
specify a sprite and a sub-image for drawing, then you must give the
*relative coordinates* within the sprite of the area to select for
drawing. This means that a left position of 0 and a top position of 0
would be the top left corner of the sprite and all further coordinates
should be taken from that position. The image below shows an example of
how this works:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/spr_part.png)  
You should note that if the texture page permits automatic cropping then
this function may not work as expected, since the extra "empty" space
around the sprite will have been removed for creating the texture page.
To resolve this issue, you will need to set the texture page settings
(in the [Texture Group Editor](../../../../Settings/Texture_Groups)
) to disable the option **Automatic Crop** . **NOTE** : When drawing
with this function, the sprite [x
offset](../../Asset_Management/Sprites/Sprite_Instance_Variables/sprite_xoffset)
and [y
offset](../../Asset_Management/Sprites/Sprite_Instance_Variables/sprite_yoffset)
are ignored and the sprite part will be drawn with the top left corner
at the specified x / y position in the room. **NOTE** : This function is
only useful for **bitmap** sprites and will not work with SWF or JSON
(Spine) sprites.

#### Syntax:

``` gml
draw_sprite_part(sprite, subimg, left, top, width, height, x, y);
```

|          |                                                                         |                                                                                                                         |
|----------|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                                                                             |
| sprite   |  [Sprite Asset](../../../../../The_Asset_Editors/Sprites)           | The index of the sprite to draw.                                                                                        |
| subimg   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The subimg (frame) of the sprite to draw (image_index or -1 correlate to the current frame of animation in the object). |
| left     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x position on the sprite of the top left corner of the area to draw.                                                |
| top      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y position on the sprite of the top left corner of the area to draw.                                                |
| width    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The width of the area to draw.                                                                                          |
| height   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The height of the area to draw.                                                                                         |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of where to draw the sprite.                                                                           |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of where to draw the sprite.                                                                           |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_sprite_part(sprite_index, image_index, 4, 0, sprite_width-16, sprite_height-16, x, y );
```

This will draw the instances assigned sprite (sprite_index) and its
current frame of animation (image_index), however it will shave a 4px
margin off the width on both sides, and an 8 pixel margin off the height
from the bottom of the original 24x24 pixel sprite.
