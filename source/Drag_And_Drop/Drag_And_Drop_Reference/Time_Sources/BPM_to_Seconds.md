#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Icons/BPM_to_Seconds.png) BPM to Seconds

This action takes a beats-per-minute value, and returns the length of
each beat in seconds. This can be used when [creating a Time
Source](Create_Time_Source) to use a BPM value for the Time Source .
It's important that such a Time Source uses **seconds** as its
[unit](../../../GameMaker_Language/GML_Reference/Time_Sources/Time_Source_Units)
.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Syntax/BPM_to_Sec.png)  

#### Arguments:

|          |                                                                |
|----------|----------------------------------------------------------------|
| Argument | Description                                                    |
| Value    | The beats-per-minute value                                     |
| Target   | The variable to store the returned seconds-per-beat value      |
| Temp     | Whether the variable should be created as a temporary variable |
