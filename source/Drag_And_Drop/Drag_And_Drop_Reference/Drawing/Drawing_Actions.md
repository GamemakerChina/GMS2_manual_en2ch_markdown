# Drawing Action Library

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/Lib_Drawing.png)  
The **Drawing** action library is where you can find the actions
required to draw sprites, text or shapes as well as set certain draw
properties. Most of these actions are **only for use in the various
[Draw
Events](../../../The_Asset_Editors/Object_Properties/Draw_Events)**
of an object, and may not work if used outside of the Draw Event. The
exceptions to this are the *Set* actions, which can be added to any
event and will affect all drawing for all instances afterwards. It is
important to note that if you add any actions into the main **Draw
Event** of an object, then it will *not* draw the sprite that has been
assigned to the instance unless you explicitly tell GameMaker to draw
it, using an action like [Draw Self](Draw_Self) . Basically,
GameMaker will default draw any sprite assigned to an instance, only if
there is *nothing* else in the Draw Event. The Draw actions available
are as follows:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Self.png" /><br />
</td>
<td><a href="Draw_Self">Draw Self</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Value.png" /><br />
</td>
<td><a href="Draw_Value">Draw Value</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Transformed_Value.png" /><br />
</td>
<td><a href="Draw_Transformed_Value">Draw Transformed Value</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Sprite.png" /><br />
</td>
<td><a href="Draw_Sprite">Draw Sprite</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Sprite_Transformed.png" /><br />
</td>
<td><a href="Draw_Sprite_Transformed">Draw Sprite
Transformed</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Stacked_Sprites.png" /><br />
</td>
<td><a href="Draw_Stacked_Sprites">Draw Stacked Sprites</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Rectangle.png" /><br />
</td>
<td><a href="Draw_Rectangle">Draw Rectangle</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Rectangle_Gradient.png" /><br />
</td>
<td><a href="Draw_Gradient_Rectangle">Draw Gradient
Rectangle</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Ellipse.png" /><br />
</td>
<td><a href="Draw_Ellipse">Draw Ellipse</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Ellipse_Gradient.png" /><br />
</td>
<td><a href="Draw_Gradient_Ellipse">Draw Gradient Ellipse</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Line.png" /><br />
</td>
<td><a href="Draw_Line">Draw Line</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Healthbar.png" /><br />
</td>
<td><a href="Draw_Healthbar">Draw Healthbar</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Instance_Score.png" /><br />
</td>
<td><a href="Draw_Instance_Score">Draw Instance Score</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Instance_Health.png" /><br />
</td>
<td><a href="Draw_Instance_Health">Draw Instance Health</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Draw_Instance_Lives.png" /><br />
</td>
<td><a href="Draw_Instance_Lives">Draw Instance Lives</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Set_Draw_Colour.png" /><br />
</td>
<td><a href="Set_Draw_Colour">Set Draw Colour</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Get_Draw_Colour.png" /><br />
</td>
<td><a href="Get_Draw_Colour">Get Draw Colour</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Set_Draw_Alpha.png" /><br />
</td>
<td><a href="Set_Draw_Alpha">Set Draw Alpha</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Get_Draw_Alpha.png" /><br />
</td>
<td><a href="Get_Draw_Alpha">Get Draw Alpha</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Set_Font.png" /><br />
</td>
<td><a href="Set_Font">Set Font</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Get_Font.png" /><br />
</td>
<td><a href="Get_Draw_Font">Get Draw Font</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Set_Text_Alignment.png" /><br />
</td>
<td><a href="Set_Text_Alignment">Set Text Alignment</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Get_Text_Alignment.png" /><br />
</td>
<td><a href="Get_Text_Alignment">Get Text Alignment</a></td>
</tr>
</tbody>
</table>
