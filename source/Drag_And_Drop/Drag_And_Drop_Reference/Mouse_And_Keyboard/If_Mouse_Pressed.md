#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Mouse_And_Keyboard/i_KeyboardMouse_Pressed.png) If Mouse Pressed

This action checks for the initial press on a mouse button. It will
return true on the single game step (frame) that the button is initially
pressed down and false at all other times. If you enable the not
modifier, this action will be reversed, and check if the button has
*not* been pressed down, returning false on the game step (frame) that
it has been pressed down and true at all other times.. If you need to
check for a button being held down and not just the initial press event,
then use the action [If Mouse Down](If_Mouse_Down) . Note that to
add actions into the "if" block, they should be dropped to the side of
the action, as shown in the image below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Mouse_And_Keyboard/a_If_Mouse_PressedDrop.png)  
These actions will now be run if the "if" evaluates to true , while any
actions dropped elsewhere will be performed after the "if" block.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Mouse_And_Keyboard/a_KeyboardMouse_Pressed.png)  

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
