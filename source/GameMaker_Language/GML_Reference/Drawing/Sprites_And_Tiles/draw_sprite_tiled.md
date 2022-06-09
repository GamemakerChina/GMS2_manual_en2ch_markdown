# draw_sprite_tiled

This function will take a sprite and then repeatedly tile it across the
whole view (or room if no view is defined), starting from the
coordinates that you give in the function. Tiling is based on the width
and height of the sprite as defined by the [sprite
variables](../../Asset_Management/Sprites/Sprite_Instance_Variables/Sprite_Instance_Variables)
of the instance running the code. This function is for 2D (orthographic)
projections only, and will not work correctly when a 3D camera
projection is used.

#### Syntax:

``` gml
draw_sprite_tiled(sprite, subimg, x, y);
```

|          |                                                                         |                                                                                                                         |
|----------|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                                                                             |
| sprite   |  [Sprite Asset](../../../../../The_Asset_Editors/Sprites)           | The index of the sprite to draw.                                                                                        |
| subimg   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The subimg (frame) of the sprite to draw (image_index or -1 correlate to the current frame of animation in the object). |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of where to draw the sprite.                                                                           |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of where to draw the sprite.                                                                           |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_sprite_tiled(sprite_index, image_index, x, y);
```

This will draw the instances assigned sprite (sprite_index) and its
current frame of animation (image_index) at the instances own x and y
position, and tiled horizontally and vertically across the view.
