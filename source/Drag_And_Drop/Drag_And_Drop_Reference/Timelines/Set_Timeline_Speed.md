#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Timelines/i_Timelines_Set_Timeline_Speed.png) Set Timeline Speed

This action can be used to set the speed at which a timeline will move
through the moments it contains. Normally, in each game frame you'd want
the position in the timeline to be increased by 1, however you can
change this amount by setting this action to a different value. The
value you choose will be treated as a *multiplier* so a value of 2, for
example, will make the timeline run at twice the speed, while a value of
0.5 would make it run at half the speed. What this means for the moments
is that if the value is greater than one, then several moments could
occur within the same game frame (no moments are ever skipped), and if
the speed is less than one, then after a moment has run, there will be
frames where nothing happens until the next moment runs - if you set the
timeline speed to 0.1, for example, you will get a moment on one game
frame, then 9 game frames with no moments, and on the tenth game frame
the next moment will be run. If you set a timeline to start using the
actions [Set Instance Timeline](Set_Instance_Timeline) or [Set
Timeline State](Set_Timeline_State) but *don't* set the speed, then
the timeline will default to 1 moment per game frame.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Timelines/a_Timelines_Set_Timeline_Speed.png)  

#### Arguments:

|          |                                                                         |
|----------|-------------------------------------------------------------------------|
| Argument | Description                                                             |
| Speed    | The speed - as a multiplier - for the timeline to run at (default is 1) |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Timelines/e_Timelines_Set_Instance_Timeline.png)  
The above action block code will assign a timeline to the instance
calling the actions as well as set the initial moment to 10 and then the
timeline speed to 2.
