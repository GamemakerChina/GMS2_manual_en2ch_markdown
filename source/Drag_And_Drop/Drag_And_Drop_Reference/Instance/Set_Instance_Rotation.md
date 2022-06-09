#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/i_Instance_Set_Rotation.png) Set Instance Rotation

This action block sets the image_angle (rotation) of the instance. The
angle is measured in degrees, with the right being 0°, up being 90°,
left being 180° and down being 270°. Set this variable to 0 to reset the
instance, meaning that it will draw any sprite assigned to as it was
defined in the sprite editor. Please note that for changes in this
action to be visible, the instance should have either *no* draw event
(and so GameMaker will default draw the sprite) or be drawn using [Draw
Self](../Drawing/Draw_Self) action.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/a_Instance_Set_Rotation.png)  

#### Arguments:

|          |                                       |
|----------|---------------------------------------|
| Argument | Description                           |
| Angle    | The new angle to use (from 0 to 360). |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/e_Instance_Set_Sprite.png)  
The above action block code sets a new sprite as well as a number of
other properties for how that sprite is to be displayed, including
rotating it 180°.
