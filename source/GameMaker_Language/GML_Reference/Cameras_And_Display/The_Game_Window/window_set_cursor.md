# window_set_cursor

With this function you can set the cursor for the game window to any one
of the constants listed below (to find the current cursor being used you
can use the function [ window_get_cursor()
](../The_Game_Window/window_get_cursor) which will also return one
of these constants):

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="header">
<th>Constant</th>
<th>Cursor</th>
</tr>

<tr class="odd">
<td><span> cr_none </span></td>
<td></td>
</tr>
<tr class="even">
<td><span> cr_default </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_Default.png" /><br />
</td>
</tr>
<tr class="odd">
<td><span> cr_arrow </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_Arrow.png" /><br />
</td>
</tr>
<tr class="even">
<td><span> cr_cross </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_Cross.png" /><br />
</td>
</tr>
<tr class="odd">
<td><span> cr_beam </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_Beam.png" /><br />
</td>
</tr>
<tr class="even">
<td><span> cr_size_nesw </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_SizeNeSw.png" /><br />
</td>
</tr>
<tr class="odd">
<td><span> cr_size_ns </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_SizeNS.png" /><br />
</td>
</tr>
<tr class="even">
<td><span> cr_size_nwse </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_SizeNwSe.png" /><br />
</td>
</tr>
<tr class="odd">
<td><span> cr_size_we </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_SizeWE.png" /><br />
</td>
</tr>
<tr class="even">
<td><span> cr_uparrow </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_Up.png" /><br />
</td>
</tr>
<tr class="odd">
<td><span> cr_hourglass </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_Hourglass.png" /><br />
</td>
</tr>
<tr class="even">
<td><span> cr_drag </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_Drag.png" /><br />
</td>
</tr>
<tr class="odd">
<td><span> cr_appstart </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_AppStart.png" /><br />
</td>
</tr>
<tr class="even">
<td><span> cr_handpoint </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_Hand.png" /><br />
</td>
</tr>
<tr class="odd">
<td><span> cr_size_all </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/cr_SizeAll.png" /><br />
</td>
</tr>
</tbody>
</table>

#### Syntax:

``` gml
window_set_cursor(cursor);
```

|          |                                                                                                                                |                                        |
|----------|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                                           | Description                            |
| cursor   |  [Cursor Constant](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/The_Game_Window/window_get_cursor)  | The cursor to set for the game window. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if mouse_check_button_pressed(mb_left)
{
    window_set_cursor(cr_drag);
}
```

The above code will change the window cursor to the standard windows
drag cursor if the left mouse button has been pressed.
