#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Rectangle_Gradient.png) Draw Gradient Rectangle

This action will draw a rectangle at a given position within the room,
using a set of blend colours to create a gradient. You give the top left
position and the bottom right position and the rectangle will be drawn
between them, and the position can either be an absolute position within
the room, or a position relative to the instance calling the action. You
then set the colours to blend from each of the corners and can also set
whether the rectangle can be filled or outlined by checking the **fill**
box at the bottom. **NOTE** : This action is only for use in the various
[Draw
Events](../../../The_Asset_Editors/Object_Properties/Draw_Events) ,
and will not draw anything if used elsewhere.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/a_Drawing_Draw_Gradient_Rectangle.png)  

#### Arguments:

|              |                                                  |
|--------------|--------------------------------------------------|
| Argument     | Description                                      |
| Left         | The left position to start drawing from          |
| Top          | The top position to start drawing from           |
| Right        | The right position to end drawing from           |
| Bottom       | The bottom position to end drawing from          |
| Top Left     | The colour to blend from the top left corner     |
| Top Right    | The colour to blend from the top right corner    |
| Bottom Left  | The colour to blend from the bottom left corner  |
| Bottom Right | The colour to blend from the bottom right corner |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/e_Drawing_Draw_Gradient_Rectangle.png)  
The above action block code draws a gradient rectangle relative to the
instance position with some text over it.
