#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Line.png) Draw Line

This action will draw a line at a given position within the room. You
give the initial x/y position and then the final x/y position and the
line will be drawn between them using the current draw colour. The
positions can either be an absolute position within the room, or a
position relative to the instance calling the action. **NOTE** : This
action is only for use in the various [Draw
Events](../../../The_Asset_Editors/Object_Properties/Draw_Events) ,
and will not draw anything if used elsewhere.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/a_Drawing_Draw_Line.png)  

#### Arguments:

|          |                          |
|----------|--------------------------|
| Argument | Description              |
| x        | The starting x position  |
| y        | The starting y position  |
| x2       | The finishing x position |
| y2       | The finishing y position |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/e_Drawing_Draw_Line.png)  
The above action block code draws a pink line across the top of the
room.
