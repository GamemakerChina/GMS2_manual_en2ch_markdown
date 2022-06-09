#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Instance_Lives.png) Draw Instance Lives

This action will draw a sprite to represent each of the lives the
instance currently have. The number to draw is taken from the current
value of the local instance variable lives , which is a special variable
that is created automatically within the instance if you use any of the
actions that require it. You give the sprite to draw for the lives and
the stack order, which can be either **Row** (horizontally, left to
right), or **column** (vertically, top to bottom), as well as the
position. The position can be an absolute position within the room, or
one relative to the position of the instance doing the drawing, and the
spacing between images will be based on the width or height of the
sprite. Note that this simply draws a static image - the initial single
image (frame 0) of the given sprite - and any further frames will be
ignored, as will any transforms that have been added to the instance
through changing the instance variables (like image_xscale or
image_blend ). Caption text will be drawn preceding the lives value and
if it is text it should be wrapped with "", and both will be formatted
using the current draw font , colour and alignment. **NOTE** : This
action is only for use in the various [Draw
Events](../../../The_Asset_Editors/Object_Properties/Draw_Events) ,
and will not draw anything if used elsewhere.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/a_Drawing_Draw_Instance_Lives.png)  

#### Arguments:

|             |                                                                                 |
|-------------|---------------------------------------------------------------------------------|
| Argument    | Description                                                                     |
| Caption     | The string to draw along with the score value (preceding and can be left blank) |
| Stack Order | The order to draw in (either Row or Column)                                     |
| x           | The x position to draw the lives at                                             |
| y           | The y position to draw the lives at                                             |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/e_Drawing_Draw_Instance_Lives.png)  
The above action block code draws sprites relative to the instance to
represent the current lives value.
