#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/i_Instance_Set_Colour.png) Set Instance Colour

This action block sets the image_blend colour for "blending" with the
instance sprite. The default value is the hex code $FFFFFFFF (which
represents the colour white using ARGB format) and this will draw the
sprite using no blending and full alpha. Any other value (including
internal colour constants like c_red , or c_aqua ) will *blend* the
specified colour with the original sprite as well as set the image_alpha
component for the instance, but only when the **Use Alpha** checkbox is
ticked. This will overwrite any alpha value set previously using the
action [Set Instance Alpha](Set_Instance_Alpha) . Please note that
for changes in this action to be visible, the instance should have
either *no* draw event (and so GameMaker will default draw the sprite)
or be drawn using [Draw Self](../Drawing/Draw_Self) action. It is
important to note too that you should try to limit blending on the
**HTML5** platform (unless using WebGL), as each blended sprite has to
be cached separately and so having many blended sprites may adversely
affect performance.  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/sprite_colour.png)  

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/a_Instance_Set_Colour.png)  

#### Arguments:

|          |                                                                                                 |
|----------|-------------------------------------------------------------------------------------------------|
| Argument | Description                                                                                     |
| Colour   | The new blending colour to use (clicking the colour swatch will open the colour picker window). |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/e_Instance_Set_Sprite.png)  
The above action block code sets a new sprite as well as a number of
other properties for how that sprite is to be displayed, including
setting the blend colour to pink.
