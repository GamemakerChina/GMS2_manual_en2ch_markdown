# layer_enable_fx

This function enables/disables the filter/effect assigned to a Room
Layer. You specify either the ID or the name of the layer you want to
modify, and then a boolean value telling whether the FX should be
enabled ( true ) or disabled ( false ). Passing in false will not remove
the FX from the layer, but simply make it invisible. Use
[layer_clear_fx()](layer_clear_fx) to remove an FX from a layer.
Similarly, passing in true will not do anything if there is no FX
applied to the layer. Use [layer_set_fx()](layer_set_fx) to apply an
FX to a layer.

#### Syntax:

``` gml
layer_enable_fx(layer_name_or_id, enable);
```

|                  |                                                                                                                                                                                                                  |                                       |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| Argument         | Type                                                                                                                                                                                                             | Description                           |
| layer_name_or_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The name or ID of the layer to modify |
| enable           |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                     | Whether to enable or disable the FX   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (hp &amp;lt;= 3)
{
    layer_enable_fx("DesaturateLayer", true);
}
else
{
    layer_enable_fx("DesaturateLayer", false);
}
```

The above code enables a Desaturate FX layer if the instance's HP value
is less than or equal to 3, otherwise it disables it. This indicates to
the player that their HP is low, by desaturating the screen.
