#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Stacked_Sprites.png) Draw Stacked Sprites

This action will draw a sprite a given number of sprites one after
another at a given position within the room. You give the sprite to draw
and the stack order, which can be either **Row** (horizontally, left to
right), or **column** (vertically, top to bottom), as well as the number
of sprites to draw and the position. The position can be an absolute
position within the room, or one relative to the position of the
instance doing the drawing, and the spacing between images will be based
on the width or height of the sprite. Note that this simply draws a
static image - the initial single image (frame 0) of the given sprite -
and any further frames will be ignored, as will any transforms that have
been added through changing the [instance
variables](../Instance/Set_Instance_Variable) (like image_xscale or
image_blend ). **NOTE** : This action is only for use in the various
[Draw
Events](../../../The_Asset_Editors/Object_Properties/Draw_Events) ,
and will not draw anything if used elsewhere.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/a_Drawing_Draw_Stacked_Sprites.png)  

#### Arguments:

|             |                                             |
|-------------|---------------------------------------------|
| Argument    | Description                                 |
| Sprite      | The sprite to draw                          |
| Stack Order | The order to draw in (either Row or Column) |
| Number      | The number of sprites to draw               |
| x           | The x position to draw at                   |
| y           | The y position to draw at                   |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/e_Drawing_Draw_Stacked_Sprites.png)  
The above action block code gets the number of instances of the object
"obj_Player" and then uses this to draw a number of marker sprites to
the screen.
