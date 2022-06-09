#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/i_Instance_Set_Sprite.png) Set Sprite

This action block sets the sprite_index of the instance to another
sprite from the Asset Browser. You select the sprite to change to, and
then give the image (animation frame) to show. Note that if you don't
want the sprite to animate after setting the frame, you'll need to use
the [Set Animation Speed](Set_Animation_Speed) action and set it to
0, or if you want the sprite to continue animating then set the value to
use the image_index built-in variable variable instead. Changing the
sprite will also change the collision mask of the instance, unless you
have also specified a separate mask_index in the [Object
Editor](../../../The_Asset_Editors/Objects) . Please note that for
changes in this action to be visible, the instance should have either
*no* draw event (and so GameMaker will default draw the sprite) or be
drawn using [Draw Self](../Drawing/Draw_Self) action.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/a_Instance_Set_Sprite.png)  

#### Arguments:

|          |                                                                                  |
|----------|----------------------------------------------------------------------------------|
| Argument | Description                                                                      |
| Sprite   | The new sprite to use (-1 if you want to remove the sprite).                     |
| Frame    | The animation frame to show initially (if no extra frames are used, then use 0). |

#### Example:

The above action block code sets a new sprite as well as a number of
other properties for how that sprite is to be displayed.
