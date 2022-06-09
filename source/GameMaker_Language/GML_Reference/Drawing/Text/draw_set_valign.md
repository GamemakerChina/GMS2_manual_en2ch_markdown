# draw_set_valign

This function is used to align text along the vertical axis and changing
the vertical alignment will change the position and direction in which
all further text is drawn, with the default value being fa_top . The
following constants are accepted:

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
<td><span> fa_top </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/fa_top.png" /><br />
</td>
</tr>
<tr class="even">
<td><span> fa_middle </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/fa_middle.png" /><br />
</td>
</tr>
<tr class="odd">
<td><span> fa_bottom </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/fa_bottom.png" /><br />
</td>
</tr>
</tbody>
</table>

#### Syntax:

``` gml
draw_set_valign(valign);
```

|          |                                                                                                                   |                                                     |
|----------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                                                              | Description                                         |
| valign   |  [Vertical Alignment Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Text/draw_set_valign)  | Vertical alignment constant (from the table above). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_halign(fa_center);
draw_set_valign(fa_middle);
draw_text(100, 32, "Score: " + string(score));
```

The above code will draw the score centered around the very center of
the text.
