#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Rooms/i_Rooms_Go_To_Room.png) Go To Room

This action will end the current room and go to the room specified by
the input index. The room must exist or else an error will be given, and
if you use the same room as the current room it will have the same
effect as using [Restart Room](Restart_Room) . Note that the room
will *not* change until the end of the event or script where the action
was called, so any actions after this one will still run.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Rooms/a_Rooms_Go_To_Room.png)  

#### Arguments:

|          |                   |
|----------|-------------------|
| Argument | Description       |
| Room     | The room to go to |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Rooms/e_Rooms_Go_To_Room.png)  
The above action block code retrieves a global variable and then checks
to see if the value it holds is less than or equal to 0. If it is then
the game will go to another room.
