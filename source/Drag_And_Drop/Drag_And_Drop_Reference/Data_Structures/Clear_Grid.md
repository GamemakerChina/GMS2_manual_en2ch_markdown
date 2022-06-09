#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/i_DS_Clear_Grid.png) Clear Grid

With this action you can clear a grid data structure to a single value
(each cell within the grid will be set to the value given). You supply
the variable that holds the grid index (as returned by the action
[Create Grid](Create_Grid) ) and then give the value to clear the
grid to.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/a_DS_Clear_Grid.png)  

#### Arguments:

|          |                                                       |
|----------|-------------------------------------------------------|
| Argument | Description                                           |
| Grid     | The index (stored in a variable) of the grid to clear |
| Value    | The value to clear the grid to                        |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/e_DS_Clear_Grid.png)  
The above action block code clears the given grid data structure to hold
the keyword noone in each cell if a global variable is less than or
equal to 0.
