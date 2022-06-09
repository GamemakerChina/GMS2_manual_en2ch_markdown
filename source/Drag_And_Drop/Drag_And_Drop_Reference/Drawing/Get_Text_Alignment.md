#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Get_Text_Alignment.png) Get Text Alignment

This action will get the font alignment for all current draw text
actions. You can choose whether to retrieve the horizontal or vertical
alignment to check, and the action will return one of the following
*constant* values, that represent a different type of horizontal or
vertical alignment:

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

The return constant will be stored in the **target variable** that you
specify, which can have been created previously or can be a new
temporary one (if you check the "Temp" check-box).

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/a_Drawing_Get_Text_Alignment.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/e_Drawing_Get_Font_Alignment.png)  
The above action block code checks the horizontal text alignment and if
it's not set to fa_left , then it is set to that value.
