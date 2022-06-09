# draw_set_halign

This function is used to align text along the horizontal axis and
changing the horizontal alignment will change the position and direction
in which all further text is drawn with the default value being fa_left
. The following constants are accepted:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="header">
<th>Constant</th>
<th>Alignment</th>
</tr>

<tr class="odd">
<td><span> fa_left </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/fa_left.png" /><br />
</td>
</tr>
<tr class="even">
<td><span> fa_center </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/fa_center.png" /><br />
</td>
</tr>
<tr class="odd">
<td><span> fa_right </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/fa_right.png" /><br />
</td>
</tr>
</tbody>
</table>

#### Syntax:

``` gml
draw_set_halign(halign);
```

|          |                                                                                                                     |                                                       |
|----------|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument | Type                                                                                                                | Description                                           |
| halign   |  [Horizontal Alignment Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Text/draw_set_halign)  | Horizontal alignment constant (from the table above). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_halign(fa_left);
draw_text(100, 32, "Score: " + string(score));
draw_set_halign(fa_right);
draw_text(room_width - 100, 32, "Health: " + string(health));
```

The above code will draw two strings on the same line, with the score
being left-hand aligned and the health being right-hand aligned.
