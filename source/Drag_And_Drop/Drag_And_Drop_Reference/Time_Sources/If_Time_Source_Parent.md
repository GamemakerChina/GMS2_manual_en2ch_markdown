#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Icons/If_Parent.png) If \[Time Source\] Parent

This action allows you to control other actions based on the parent of
the given Time Source . It checks if the Time Source given in "Parent"
is (or isn't) the parent of the Time Source given in "Time Source".

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Syntax/If_TS_Parent.png)  

#### Arguments:

|             |                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Argument    | Description                                                                                                                                                                  |
| Time Source | The [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create) to check the parent of                                                |
| Not         | Enable this to invert the condition                                                                                                                                          |
| Parent      | The [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create) to compare against the parent of the previously given Time Source     |
