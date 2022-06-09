#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Paths/i_Paths_Get_Path_Follow_Speed.png) Get Path Follow Speed

This action will get the speed, in pixels per game frame, that an
instance is set to follow a path (note that you must have called the
[Start Following Path](Start_Following_Path) action to assign a path
to the instance for this to to return a value other than 0). The
returned value will be stored in the target variable you give, or you
can flag the variable as a temporary local variable to create it and
assign the value.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Paths/a_Paths_Get_Path_Follow_Speed.png)  

#### Arguments:

|          |                                                            |
|----------|------------------------------------------------------------|
| Argument | Description                                                |
| Target   | The target variable to hold the returned path follow speed |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Paths/e_Paths_Get_Path_Follow_Speed.png)  
The above action block code gets the current speed of the instance along
the assigned path and if it's less than 4, it increments the path speed
by 0.1.
