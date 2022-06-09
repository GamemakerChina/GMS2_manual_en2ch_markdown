# draw_skeleton_collision

This function will draw the collision masks associated with the given
skeletal animation. You supply the base sprite, the animation set to use
and the frame to get the information from, and you can also set the
transform properties to suit. NOTE The bounding box of a Spine sprite is
set up in Spine itself, not in GameMaker .

#### Syntax:

``` gml
draw_skeleton_collision(sprite, animname, frame, x, y, xscale, yscale, rot, colour)
```

|          |                                                                                                                 |                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                            | Description                                                                                   |
| sprite   |  [Sprite Asset](../../../../../../../The_Asset_Editors/Sprites)                                             | The index of the sprite to draw.                                                              |
| animname |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                  | The name of the animation to get the frame from (a string).                                   |
| frame    |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The animation frame to draw (from 0 to image_number - 1).                                     |
| x        |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x coordinate of where to draw the sprite.                                                 |
| y        |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y coordinate of where to draw the sprite.                                                 |
| xscale   |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The horizontal scaling of the sprite, as a multiplier: 1 = normal scaling, 0.5 is half etc... |
| yscale   |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The vertical scaling of the sprite, as a multiplier: 1 = normal scaling, 0.5 is half etc...   |
| rot      |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The rotation of the sprite. 0=normal, 90=turned 90 degrees counter-clockwise etc.             |
| colour   |  [Colour](../../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour with which to blend the sprite.                                                    |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_skeleton_collision(sprite_index, "jump", image_index, x, y, image_xscale, image_yscale, image_angle, c_white);
```

The above code will draw the collision mask data for the current sprite,
using the current transforms, for the animation set "jump".
