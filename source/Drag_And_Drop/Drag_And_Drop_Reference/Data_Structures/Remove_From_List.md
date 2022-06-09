#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/i_DS_Remove_From_List.png) Remove From List

This action can be used to remove an index item from the given list. You
supply the variable that stores the list index (as returned by the
action [Create List](Create_List) ) and the index position within
the list to remove, where the index position is between 1 and (list
length -1). This action does not return anything so if you need the
value at the index position you should use [Get List Item
At](Get_List_Item_At) before removing the index.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/a_DS_Remove_From_List.png)  

#### Arguments:

|          |                                                             |
|----------|-------------------------------------------------------------|
| Argument | Description                                                 |
| List     | The index (stored in a variable) of the list to remove from |
| Index    | The index within the list to remove                         |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/e_DS_Remove_From_List.png)  
The above action block code checks for a collision at the instance
position and if one is found the unique ID value for the instance is
stored in a temporary variable and then checked to see if it exists
within the list data structure. If it does exist then the item is
removed from the list and the instance destroyed.
