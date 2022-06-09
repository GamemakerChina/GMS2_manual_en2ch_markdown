#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Loops/i_Loops_Loop.png) Loop

The **Loop** action will loop infinitely until a [Break](Break)
action is called. Care should be taken with this action to ensure that
regardless of the actions placed within the loop, a Break will *always*
be called, otherwise the game will cause a "not responding" error on the
target OS and stop working. You add this action into the action code
workspace and then add the actions to be performed within the loop, much
as you would add an action to an "if", ie: dropping it to the side of
the action rather than under it:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Loops/Loop_Drop.png)  

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Loops/a_Loops_Loop.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Loops/e_Loops_Loop.png)  
The above action block code will loop until the instance variable count
is greater than or equal to 10, at which point it will break and then
continue with any further actions outside the loop.
