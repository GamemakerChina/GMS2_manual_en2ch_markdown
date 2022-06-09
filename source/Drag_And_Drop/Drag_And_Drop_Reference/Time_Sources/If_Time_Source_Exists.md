#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Icons/If_Time_Source_Exists.png) If Time Source Exists

This action allows you to control other actions based on whether the
given Time Source exists or not.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Syntax/If_TS_Exists.png)  

#### Arguments:

|             |                                                                                                                   |
|-------------|-------------------------------------------------------------------------------------------------------------------|
| Argument    | Description                                                                                                       |
| Time Source | The [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create) to check   |
| Not         | Enable this to run connected actions if the Time Source does *not* exist                                          |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Examples/Eg_Destroy_TS.png)  
This checks if a Time Source exists, and if it does, it destroys it.
