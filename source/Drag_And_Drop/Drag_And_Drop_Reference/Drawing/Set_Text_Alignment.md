#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Set_Text_Alignment.png) Set Text Alignment

This action will set the font alignment for all subsequent draw text
actions. You can set the horizontal alignment to be the left, center or
right, and the vertical alignment to be top, middle or bottom and the
text will be aligned relative to the x/y position of the draw action, as
shown in the images below:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/fa_left.png" /><br />
</td>
<td>Text is horizontally aligned to the left</td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/fa_center.png" /><br />
</td>
<td>Text is horizontally aligned to the center</td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/fa_right.png" /><br />
</td>
<td>Text is horizontally aligned to the right</td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/fa_top.png" /><br />
</td>
<td>Text is vertically aligned to the top</td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/fa_middle.png" /><br />
</td>
<td>Text is vertically aligned to the middle</td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/fa_bottom.png" /><br />
</td>
<td>Text is vertically aligned to the bottom</td>
</tr>
</tbody>
</table>

Note that this will set the alignment to use for *all* subsequent draw
text calls, and so can be called, for example, once at the beginning of
the game - in any event, not just the Draw Event - and all draw text
actions will use the set alignment. However if you require multiple draw
text actions to align in different ways, then you will need to call this
action before every draw text action you wish to align differently.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/a_Drawing_Set_Text_Alignment.png)  

#### Arguments:

|          |                                                      |
|----------|------------------------------------------------------|
| Argument | Description                                          |
| H.Align  | The horizontal alignment value (Left, Center, Right) |
| V.Align  | The vertical alignment value (Top, Middle, Bottom)   |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/e_Drawing_Draw_Value.png)  
The above action block code sets the font, the draw colour, and the
alignment for some text that is drawn.
