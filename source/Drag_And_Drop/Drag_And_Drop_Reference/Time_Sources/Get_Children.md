#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Icons/Get_Children.png) Get Children

This action returns an array containing all the child Time Source s for
the given Time Source . The resulting array is stored in the Target
variable.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Action_Syntax/Get_Children.png)  

#### Arguments:

|             |                                                                                                                                 |
|-------------|---------------------------------------------------------------------------------------------------------------------------------|
| Argument    | Description                                                                                                                     |
| Time Source | The [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create) to get the children of   |
| Target      | The variable to store the array                                                                                                 |
| Temp        | Whether the variable should be created as a temporary variable                                                                  |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Time_Sources/Examples/Eg_Get_Children.png)  
This gets the children for a Time Source , and loops through the array
to destroy each child Time Source . At the end it destroys the parent
Time Source . This is necessary for destroying parent Time Source s, as
you cannot destroy a Time Source that has existing children.
