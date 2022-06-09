#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Gamepad/i_GamePad_Get_Count.png) Get Gamepad Count

You can use this action to get the number of gamepads connected to the
device running your game. The number returned will be between 0 and 12.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Gamepad/a_GamePad_Get_Count.png)  

#### Arguments:

|          |                                                     |
|----------|-----------------------------------------------------|
| Argument | Description                                         |
| Target   | The target variable to store the returned value in. |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Gamepad/e_GamePad_Get_Count.png)  
The above action block code gets the number of gamepads connected and
assigns the value to a temporary local variable. This is then checked to
see if it is more than 0 and a global variable set accordingly.
