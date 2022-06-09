#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Miscellaneous/i_Misc_Show_Debug_Message.png) Show Debug Message

With this action you can send a debug message to the [Compiler
Output](../../../Introduction/The_Output_Window) . This message can
be either a string or a real number, but if you wish to use both then
the number *must be converted to a string* (see the action [Number To
String](../Data_Types/Number_To_String) ). Note that you can output
multiple messages using this action by clicking the  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Icon_Expand_Arguments.png)  
icon to expand the action with further output fields.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Miscellaneous/a_Misc_Show_Debug_Message.png)  

#### Arguments:

|          |                                          |
|----------|------------------------------------------|
| Argument | Description                              |
| Message  | The message to show in the Output window |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Miscellaneous/e_Misc_Show_Debug_Message.png)  
The above action block code will check a variable and if it returns true
then a couple of debug messages will be shown in the Output window.
