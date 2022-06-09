#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/i_DS_Set_Grid_Value.png) Set Grid Value

With this action you can set a specific cell within the grid data
structure to a value. You supply the variable that holds the grid index
(as returned by the action [Create Grid](Create_Grid) ) and then
give the x and y position (the column and row) for the cell to set, and
then finally the value for that cell. The value can be any valid data
type, but the x and y position must be whole integers within the bounds
of the grid.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/a_DS_Set_Grid_Value.png)  

#### Arguments:

|          |                                                        |
|----------|--------------------------------------------------------|
| Argument | Description                                            |
| Grid     | The index (stored in a variable) of the grid to set    |
| x        | The cell position along the x axis to set (the column) |
| y        | The cell position along the y axis to set (the row)    |
| Value    | The value to set the grid cell to                      |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/e_DS_Set_Grid_Value.png)  
The above action block code creates a new grid data structure and holds
its index value in a global variable. It then iterates through all the
instances in the room and adds their unique ID value into the cell that
corresponds to their position.
