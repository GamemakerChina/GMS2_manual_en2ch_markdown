#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Icons/Pause_Time_Source.png) Pause Time Source

This action pauses the given Time Source . You can resume it later using
[Start Time Source](Start_Time_Source) .

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Syntax/Pause_Time_Source.png)  

#### Arguments:

|             |                                                                                                                   |
|-------------|-------------------------------------------------------------------------------------------------------------------|
| Argument    | Description                                                                                                       |
| Time Source | The [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create) to pause   |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Examples/Eg_Pause_TS.png)  
This code block would ideally run in a Key Press event. It checks if the
state of a Time Source is "active", and in that case, it pauses that
Time Source . However, if the state is "paused", it starts the Time
Source again.
