#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Movement/i_Movement_Reverse.png) Reverse

This action is used to reverse certain values related to direction and
movement. The available options are:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Movement/Reverse_Options.png)  
Reversing *direction* will simply add 180° to the current direction
(looping around 360° if necessary, so, for example, reversing 270° would
give you 90°), reversing the *horizontal* or *vertical* speed will
simply multiply the given speed vector by -1, and choosing *gravity*
will do the same as choosing direction, only for the gravity direction.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Movement/a_Movement_Reverse.png)  

#### Arguments:

|           |                          |
|-----------|--------------------------|
| Argument  | Description              |
| direction | The direction to reverse |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Movement/e_Movement_Reverse.png)  
The above action block code checks for a collision of the instance with
" obj_Wall " relative to the current position to the left and to the
right. If one is found then the horizontal speed is reversed. It then
does the same for above and below the instance, reversing the vertical
speed if a collision is detected.
