#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Icons/Destroy_Time_Source.png) Destroy Time Source

This action destroys the given Time Source . You cannot destroy a Time
Source if it has existing [children](Get_Children) . Destroy the
child Time Source s first before destroying a parent (
[example](Get_Children) ).

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Syntax/Destroy_Time_Source.png)  

#### Arguments:

|             |                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------|
| Argument    | Description                                                                                                         |
| Time Source | The [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create) to destroy   |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Examples/Eg_Destroy_TS.png)  
This checks if a Time Source exists, and if it does, it destroys it.
