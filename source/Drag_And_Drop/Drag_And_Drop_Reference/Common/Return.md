#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Common/i_Common_Return.png) Return

This action is for use when creating [Action Block
Functions](../../Drag_And_Drop_Overview/Action_Block_Functions) and
is used to return a value to the instance calling the script. The return
value can be anything that a variable can hold - like a string, a
numeric value, a pointer or a resource ID - or it can be a variable
itself. Note that when we call the return action in a function, the
function will be exited - returning the given value - and **no further
actions after the return will be called** , although if you have actions
in the **event** after you call the function, these will still be run.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Common/a_Common_Return.png)  

#### Arguments:

|          |                   |
|----------|-------------------|
| Argument | Description       |
| Return   | The return value. |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Common/e_Common_Return.png)  
The above action block function sets a temporary variable to the keyword
[ noone
](../../../GameMaker_Language/GML_Overview/Instance_Keywords) , and
then checks an input variable to see what value it currently has. If the
variable is greater than 100, then an instance is created and its unique
instance ID is stored in the temporary variable, which is then returned
from the function.
