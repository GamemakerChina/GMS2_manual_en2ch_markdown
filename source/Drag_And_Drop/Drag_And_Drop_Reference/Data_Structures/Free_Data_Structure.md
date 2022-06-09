#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/i_DS_Free_Data_Structure.png) Free Data Structure

This action will free the data structure from memory and should be
called whenever a data structure is no longer required, for example in
the Destroy even of an instance or the Room End event, etc... Freeing a
data structure means that no further actions can be used to reference it
as it will no longer exist, although you can also check for this using
the action [If Data Structure Exists](If_Data_Structure_Exists) .
Note that unless the data structure has an index assigned to a global
scope variable, it will not be carried across from one room to another.
For example, if you create a player instance and a list data structure
is assigned to a variable in that instance, the list will need to be
freed if the player is destroyed *or* if the room changes with the
player instance in it (unless the player instance is flagged as
persistent), so the player instance would have two Free Data Structure
actions in it for both those events. It is important that all created
data structures are destroyed in this way when no longer required to
prevent memory leaks which can cause performance issues or even crash
your game.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/a_DS_Free_Data_Structure.png)  

#### Arguments:

|          |                                                                       |
|----------|-----------------------------------------------------------------------|
| Argument | Description                                                           |
| Type     | The type of data structure you are freeing (List, Map, Grid or Stack) |
| Variable | The variable holding the index of the data structure to free          |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/e_DS_Free_Data_Structure.png)  
The above action block code gets the size of the list referenced in the
global variable and then uses a for loop to loop through it and destroy
the instances with the IDs stored in the list. After the loop is
finished, the list is freed from memory.
