#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Movement/i_Movement_Set_Direction_Variable.png) Set Direction Variable

This action is used to set a direction for the instance that is *not*
fixed to 45° increments. You supply the direction value from 0° to
360° - where right is 0°, up is 90°, left is 180° and down is 270° - and
you can also set the *relative* flag to add/subtract the value you give
to the current direction.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Movement/a_Movement_Set_Direction_Variable.png)  

#### Arguments:

|           |                                                                          |
|-----------|--------------------------------------------------------------------------|
| Argument  | Description                                                              |
| Direction | Direction from 0° to 360° (values outside of the range will be wrapped). |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Movement/e_Movement_Set_Direction_Variable.png)  
The above action block code checks to see if the left mouse button is
being held down and if it is it sets the direction to a random value
from 0 to 360 and the speed to 5.
