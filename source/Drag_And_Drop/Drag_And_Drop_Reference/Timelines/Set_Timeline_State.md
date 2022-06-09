#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Timelines/i_Timelines_Set_Timeline_State.png) Set Timeline State

This action can be used to start, stop, pause or resume a timeline. The
timeline must first have been set for the instance using the action [Set
Instance Timeline](Set_Instance_Timeline) , and then you can use
this action at any time to change its running state from the following
options

|        |                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------|
| Option | Description                                                                                                                  |
| Start  | Start the timeline assigned to the instance (if the timeline was paused this will set the start position to moment 0 again). |
| Resume | Resume a paused timeline (if the timeline was stopped and not paused this will do nothing).                                  |
| Paused | Pause the timeline assigned to the instance (while paused the moments in a timeline will not advance with the game frames).  |
| Stop   | Stop the timeline assigned to the instance.                                                                                  |

#### Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Timelines/a_Timelines_Set_Timeline_State.png)  

#### Arguments:

|          |                                                        |
|----------|--------------------------------------------------------|
| Argument | Description                                            |
| State    | The state to put the timeline in (see the table above) |

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Timelines/e_Timelines_Set_Timeline_State.png)  
The above action block code will check the value held in a global
variable and if it is true then the timeline is paused, and if it is
false then the timeline will be resumed.
