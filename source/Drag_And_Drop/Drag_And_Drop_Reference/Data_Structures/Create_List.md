#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/i_DS_Create_List.png) Create List

This action will create a new **list** data-structure and return the
index value so you can later access the list through the other Data
Structure actions. The list index will be returned to the Target
Variable that you supply, which can have been created earlier using
either [Assign Variable](../Common/Assign_Variable) or [Declare
Temp](../Common/Declare_Temporary_Variable) , or you can flag the
"Temp" checkbox to name and create a temporary local variable to store
the value until the end of the script or event. A newly created list
data structure is considered "empty", ie: it contains no list entries.
Note that you can create additional DS lists by clicking the plus icon
  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Icon_Expand_Arguments.png)  
beside the action, and selecting another variable to hold the list ID.
**IMPORTANT!** Creating any data structure uses up memory on the target
platform, and as such all data structures should be free when no longer
needed using the action [Free Data Structure](Free_Data_Structure)
otherwise you get a memory leak which can impair your games performance
or even cause it to crash. This is particularly relevant when using
temporary local variables to store data structure indices, as these
variables are removed at the end of the code or event, but that does not
mean the data structure is removed too! The data structure will still
exist, only you will have no way to reference it, so either use an
instance variable and free the structure at a later time, or free the
structure before the end of the event or function if its index is stored
in a temporary variable.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/a_DS_Create_List.png)  

#### Arguments:

|          |                                                |
|----------|------------------------------------------------|
| Argument | Description                                    |
| Target   | The target variable to store the list index in |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Data_Structures/e_DS_Create_List.png)  
The above action block code creates a global scope variable and then
creates a new list data structure, assigning its index value to the
global variable. The scope is then changed to so all the instances of
the object "obj_Enemy_Parent" add their unique instance ID value into
the list.
