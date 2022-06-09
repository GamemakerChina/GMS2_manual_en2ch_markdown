#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Rooms/i_Rooms_If_Room_Is_Last.png) If Room Is Last

This action will check to see if the current room is the last room as
listed in the [Room Manager](../../../Settings/The_Room_Manager) .
The action will return true if the current room is the last in the Room
Manager and false if it is not. You can flag the *not* checkbox to turn
this into "If Room Is NOT Last". Note that to add actions into the "if"
block, they should be dropped to the side of the action, as shown in the
image below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Rooms/Room_Is_Last_Drop.png)  
These actions will now be run if the "if" evaluates to true , while any
actions dropped elsewhere will be performed after the "if" block.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Rooms/a_Rooms_If_Room_Is_Last.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Rooms/e_Rooms_If_Room_Is_Last.png)  
The above action block code checks to see if the current room is *not*
the last one as listed in the Room Manager. If it is not then the game
will go to the next room in the Asset Browser, otherwise it will go to a
specific room.
