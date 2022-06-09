# draw_get_valign

This function is used to get the text alignment setting along the
vertical axis, and will return one of the constants listed below.

#### Syntax:

``` gml
draw_get_valign();
```

#### Returns:

``` gml
 Constant
```

<table>
<tbody>
<tr class="header">
<th><span> <a
href="../../../../../GameMaker_Language/GML_Reference/Drawing/Text/draw_set_valign">Vertical
Alignment Constant</a> </span></th>
<th></th>
</tr>
<tr class="odd">
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

#### Example:

``` gml
var _cur_halign = draw_get_halign();
var _cur_valign = draw_get_valign();

draw_set_halign(fa_right);
draw_set_valign(fa_bottom);

draw_text(100, 32, "Score: " + string(score));

draw_set_halign(_cur_halign);
draw_set_valign(_cur_valign);
```

The above code saves the currently applied "halign" and "valign" values
to local variables, and then changes the alignments to draw some text.
After drawing it, it resets the alignments back to the values stored in
the local variables.
