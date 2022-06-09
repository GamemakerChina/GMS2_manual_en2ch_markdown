#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Icons/If_State.png) If \[Time Source\] State

This action allows you to control other actions based on the state of
the given Time Source . It checks if the [Time Source State
Constant](../../../../GameMaker_Language/GML_Reference/Time_Sources/Time_Source_States)
given in "State" is (or isn't) the state of the Time Source given in
"Time Source".

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Syntax/If_TS_State.png)  

#### Arguments:

|             |                                                                                                                                       |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Argument    | Description                                                                                                                           |
| Time Source | The [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create) to check the state of          |
| Not         | Enable this to invert the condition                                                                                                   |
| State       | The [Time Source State Constant](../../../../GameMaker_Language/GML_Reference/Time_Sources/Time_Source_States) to check against   |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Examples/Eg_Pause_TS.png)  
This code block would ideally run in a Key Press event. It checks if the
state of a Time Source is "active", and in that case, it pauses that
Time Source . However, if the state is "paused", it starts the Time
Source again.
