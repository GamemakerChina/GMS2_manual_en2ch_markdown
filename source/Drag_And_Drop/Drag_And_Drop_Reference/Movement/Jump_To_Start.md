#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Movement/i_Movement_Jump_To_Start.png) Jump To Start

This action is used to move an instance from its current position to the
position where it was originally created. The original position where an
instance is created is stored in two [instance
variables](../Instance/Get_Instance_Variable) called xstart and
ystart . These variables can be used in any other action and can also be
set to change the recorded start position.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Movement/a_Movement_Jump_To_Start.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Movement/e_Movement_Jump_To_Start.png)  
The above action block code checks to see if the top of the instances
bounding box is below the room height and if it is it moves the instance
back to the position it was created at.
