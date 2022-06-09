#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Gamepad/i_GamePad_If_Button_Pressed.png) If Gamepad Button Pressed

With this action you can poll the gamepad to see if any button is
currently being pressed. The action will return true every step that the
gamepad button is being pressed (and held) down, or false otherwise,
although if you click the not modifier you can then check to see if the
button is *not* being pressed, ie: the action will return true while no
button is pressed and false if there is. If you only need to check for a
single button press then use the action [if gamepad button
down](If_Gamepad_Button_Down) . If the button being checked is an
analogue button, then the press will not be detected until the button
value has gone above the threshold set using the action [Set Gamepad
Button Threshold](Set_Gamepad_Button_Threshold) . Note that to add
actions into the "if" block, they should be dropped to the side of the
action, as shown in the image below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Gamepad/a_If_Gamepad_Button_PressedDrop.png)  
These actions will now be run if the "if" evaluates to true , while any
actions dropped elsewhere will be performed after the "if" block.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Gamepad/a_GamePad_If_Button_Pressed.png)  

#### Arguments:

|          |                                                      |
|----------|------------------------------------------------------|
| Argument | Description                                          |
| Gamepad  | The gamepad index.                                   |
| Button   | The name of the button to check.                     |
| Not      | Negate the check (true becomes false and vice versa) |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Gamepad/e_GamePad_If_Button_Down.png)  
The above action block code polls the button state of gamepad 0 every
step and if a button is being held down it checks for the initial button
down press. If the check is true on the initial down press, a sound is
played, then, while the button is held down, the instance speed is set
to 10. If the button is not being held down, a check is done on the
button release to reset the speed to 0 again.
