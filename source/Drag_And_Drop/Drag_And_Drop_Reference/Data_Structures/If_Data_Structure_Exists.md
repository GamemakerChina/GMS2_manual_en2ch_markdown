#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/i_DS_If_Data_Structure_Exists.png) If Data Structure Exists

With this action you can check a variable to see if it indexes a data
structure or not . You first need to pick the type of data structure to
check for (either a List, a Map, a Grid or a Stack) and then you supply
the variable that holds the data structure index (as returned by the
actions [Create List](Create_List) , [Create Map](Create_Map) ,
[Create Grid](Create_Grid) , and [Create Stack](Create_Stack) ).
The action will return true if the data structure exists, and false if
it does not. Note that you can flag "not" in the action to check if a
variable does *not* hold a data structure index. Note that to add
actions into the "if" block, they should be dropped to the side of the
action, as shown in the image below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/If_Exists_Drop.png)  
These actions will now be run if the "if" evaluates to true , while any
actions dropped elsewhere will be performed after the "if" block.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/a_DS_If_Data_Structure_Exists.png)  

#### Arguments:

|           |                                                                    |
|-----------|--------------------------------------------------------------------|
| Argument  | Description                                                        |
| Structure | The type of data structure to check for (List, Map, Grid or Stack) |
| Variable  | The variable holding the data structure index                      |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/e_DS_If_Data_Structure_Exists.png)  
The above action block code checks to see if the given data structure
exists and if it does it is freed from memory.
