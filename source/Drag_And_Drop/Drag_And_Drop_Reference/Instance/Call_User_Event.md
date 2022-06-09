#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/i_Instance_Call_User_Event.png) Call User Event

With this action you can call any of the 12 available [Other - User
Events](../../../The_Asset_Editors/Object_Properties/Object_Events)
. A User Event is one that you can add scripts or action code to and
then call at any time using this action, making them essentially custom
object events.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/a_Instance_Call_Event.png)  

#### Arguments:

|          |                                                |
|----------|------------------------------------------------|
| Argument | Description                                    |
| Event    | The number of the user event to call (0 - 11). |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/e_Instance_Call_Event.png)  
The above action block code checks a variable and then calls either User
Event \[0\] or User Event \[1\] depending on whether the check evaluates
to true or false .
