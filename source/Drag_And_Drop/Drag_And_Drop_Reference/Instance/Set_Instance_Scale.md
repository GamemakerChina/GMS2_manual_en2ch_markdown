#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/i_Instance_Set_Scale.png) Set Instance Scale

This action block sets the image_xscale and image_yscale values for the
instance. The input values here are modifiers which will be applied to
the sprite assigned to the instance, where a scale of 1 (the default
value) indicates no scaling (1:1), smaller values will scale down (0.5,
for example, will half the width of the sprite), and larger values will
scale up. You can use negative values to flip the sprite and scale it
unless the value used is exactly -1 (in which case the sprite is just
flipped or mirrored about its origin with no scaling). You can choose to
set the horizontal or vertical scale relative to the current values, in
which case you will be adding or subtracting the new value from the
current scale values. Note that changing these values will also change
how the instance detects collisions, unless you have supplied a separate
mask_index (collision mask) in the [Object
Editor](../../../The_Asset_Editors/Objects) . Please note that for
changes in this variable to be visible, the instance should have either
*no* draw event (and so GameMaker will default draw the sprite) or be
drawn using [Draw Self](../Drawing/Draw_Self) action.  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/sprite_scale.png)  

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/a_Instance_Set_Scale.png)  

#### Arguments:

|            |                                                      |
|------------|------------------------------------------------------|
| Argument   | Description                                          |
| Horizontal | The vertical scaling factor to use (default is 1).   |
| Vertical   | The horizontal scaling factor to use (default is 1). |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/e_Instance_Set_Sprite.png)  
The above action block code sets a new sprite as well as a number of
other properties for how that sprite is to be displayed, including
setting it to scale to three quarters of its base size along both axis.
