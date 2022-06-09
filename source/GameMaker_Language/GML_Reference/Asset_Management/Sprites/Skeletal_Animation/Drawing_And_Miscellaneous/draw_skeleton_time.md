# draw_skeleton_time

This function will draw the given animation using the given skin at a
specific time in the animation. The time value should be between 0 (the
beginning) and the end duration of the animation, which you can find
using the function [ skeleton_animation_get_duration()
](../Animation/skeleton_animation_get_duration) . You *can* set the
time value to values higher than the total duration of the animation and
the animation will loop back to the beginning, but you run the risk of
losing floating point accuracy as the accumulated time gets larger.

#### Syntax:

``` gml
draw_skeleton_time(sprite, animname, skinname, time, x, y, xscale, yscale, rot, colour)
```

|          |                                                                                                                 |                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                            | Description                                                                                   |
| sprite   |  [Sprite Asset](../../../../../../../The_Asset_Editors/Sprites)                                             | The index of the sprite to draw.                                                              |
| animname |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                  | The name of the animation to get the frame from (a string).                                   |
| skinname |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                  | The name of the skin to use for drawing (a string).                                           |
| time     |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The time-frame to draw the animation at (from 0 to the end duration, in seconds).             |
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
var time += delta_time / 1000000;
var d = skeleton_animation_get_duration("walk");
if time &amp;gt; d time -= d;
draw_skeleton_time(sprite_index, "walk", "skin1", time, x, y, image_xscale, image_yscale, image_angle, c_white);
```

The above code will draw the given skeletal animation sprite using
delta-time to set the frame being drawn.
