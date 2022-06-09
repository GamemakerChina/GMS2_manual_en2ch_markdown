#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Gamepad/i_GamePad_Set_Button_Threshold.png) Set Gamepad Button Threshold

This action can be used to set the "threshold" of the gamepad analogue
buttons. You specify the gamepad index to set, and then set a value from
0 to 1 and if the analogue button input amount is lower than the given
value, the gamepad button is considered to be at 0. Note that this is a
*global* setting that will affect *all* analogue buttons connected
gamepad. This value will be used in all
[down](If_Gamepad_Button_Down) ,
[pressed](If_Gamepad_Button_Pressed) and
[released](If_Gamepad_Button_Released) checks for the given gamepad,
but will be *ignored* by the action [Get Gamepad
Trigger](Get_Gamepad_Trigger) .

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Gamepad/a_GamePad_Set_Button_Threshold.png)  

#### Arguments:

|          |                             |
|----------|-----------------------------|
| Argument | Description                 |
| Gamepad  | The gamepad index.          |
| Deadzone | The threshold value (0 - 1) |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Gamepad/e_GamePad_Set_Button_Threshold.png)  
The above action block code sets the button threshold for all gamepad
indices to 0.2.
