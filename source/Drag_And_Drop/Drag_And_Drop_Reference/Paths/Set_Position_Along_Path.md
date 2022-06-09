#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Paths/i_Paths_Set_Position_Along_Path.png) Set Position Along Path

This action will set the position of an instance along a path. The value
is normalised from 0 - 1, so if you set it to, for example, 0.5, the
instance will be moved to exactly the middle of the path. Note that you
must have called the [Start Following Path](Start_Following_Path)
action to assign a path to the instance for this to have any effect.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Paths/a_Paths_Set_Position_Along_Path.png)  

#### Arguments:

|          |                                                                |
|----------|----------------------------------------------------------------|
| Argument | Description                                                    |
| Position | The position (from 0 - 1) along the path to place the instance |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Paths/e_Paths_Set_Position_Along_Path.png)  
The above action block code starts the instance along a path and then
generates a random decimal value between 0 and 1. This value is stored
in a temporary local variable and used to set the position of the
instance along the path.
