#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Mouse_And_Keyboard/i_KeyboardMouse_Released.png) If Mouse Released

This action checks for when a mouse button has been released. It will
return true on the single game step (frame) that the mouse button is
released on and false at all other times. If you enable the not
modifier, this action will be reversed, and check if the mouse button
has *not* been released, returning false on the game step (frame) that
it has been released on and true at all other times. Note that to add
actions into the "if" block, they should be dropped to the side of the
action, as shown in the image below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Mouse_And_Keyboard/a_If_Mouse_ReleasedDrop.png)  
These actions will now be run if the "if" evaluates to true , while any
actions dropped elsewhere will be performed after the "if" block.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Mouse_And_Keyboard/a_KeyboardMouse_Released.png)  

#### Arguments:

|              |                                                                                                                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Argument     | Description                                                                                                                                                                                |
| Mouse Button | The name of the mouse button to check ( *[see this page](../../../GameMaker_Language/GML_Reference/Game_Input/Mouse_Input/Mouse_Input)* *for information on mouse button constants* ). |
| Not          | Negate the check (true becomes false and vice versa)                                                                                                                                       |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Mouse_And_Keyboard/e_KeyboardMouse_Down.png)  
The above action block code polls the mouse button state every step and
if it is being held down it checks for the initial mouse down press. If
the check is true on the initial down press the instance speed is set,
then, while the button is down, the sprite blending is changed to red.
If the mouse is not being held down, a check is done on the mouse
release to reset the blending colour to white and set the speed to 0.
