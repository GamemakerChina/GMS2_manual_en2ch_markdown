#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/i_Instance_Set_Alpha.png) Set Instance Alpha

This action block sets the image_alpha value for the instance. The image
alpha is the "transparency" value for drawing any sprite assigned to the
instance and has a value between 0 and 1, where 0 would be fully
transparent and 1 would be fully opaque. Note that if the sprite has
transparent or semi-transparent pixels, then their transparency will be
scaled by the amount, so if you have some 50% transparent pixels in the
sprite and set the instance alpha to 0.5, the final alpha for the
transparent pixels would be 25%. You can set this value to be a relative
amount Please note that for changes in this variable to be visible, the
instance should have either *no* draw event (and so GameMaker will
default draw the sprite) or be drawn using [Draw
Self](../Drawing/Draw_Self) action.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/a_Instance_Alpha.png)  

#### Arguments:

|          |                                                     |
|----------|-----------------------------------------------------|
| Argument | Description                                         |
| alpha    | The alpha value to set (from 0 to 1, default is 1). |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/e_Instance_Set_Sprite.png)  
The above action block code sets a new sprite as well as a number of
other properties for how that sprite is to be displayed, including
setting the image alpha to be 0.5.
