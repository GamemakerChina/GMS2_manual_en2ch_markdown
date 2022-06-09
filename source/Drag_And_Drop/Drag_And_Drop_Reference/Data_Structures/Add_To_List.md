#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/i_DS_Add_To_List.png) Add To List

This action can be used to add a new value (of any data type) to the
list, and this value will be added on at the end. You supply the
variable that stores the list index (as returned by the action [Create
List](Create_List) ) and the value to store.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/a_DS_Add_To_List.png)  

#### Arguments:

|          |                                                        |
|----------|--------------------------------------------------------|
| Argument | Description                                            |
| List     | The index (stored in a variable) of the list to add to |
| Value    | The value to add into the list                         |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/e_DS_Create_List.png)  
The above action block code creates a global scope variable and then
creates a new list data structure, assigning its index value to the
global variable. The scope is then changed to so all the instances of
the object "obj_Enemy_Parent" add their unique instance ID value into
the list.
