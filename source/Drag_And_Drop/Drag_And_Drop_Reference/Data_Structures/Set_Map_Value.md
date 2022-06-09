#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/i_DS_Set_Map_Value.png) Set Map Value

With this action you can add a key/value pair into the map data
structure. You supply the variable that holds the map index (as returned
by the action [Create Map](Create_Map) ) and then give a "key"
(which is the identifier within the map for a value), and then the
"value" to be associated with that key. Both keys can be either integer
values (like 0, 200, 36712, etc...) or strings (like "Name", "Shield"
etc...), but the value can be any valid data type.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/a_DS_Set_Map_Value.png)  

#### Arguments:

|          |                                                    |
|----------|----------------------------------------------------|
| Argument | Description                                        |
| Map      | The index (stored in a variable) of the map to set |
| Key      | The key to set (integer or string)                 |
| Value    | The value to be stored with the given key          |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/e_DS_Set_Map_Value.png)  
The above action block code creates a new map data structure and then
sets three key/value entries in it.
