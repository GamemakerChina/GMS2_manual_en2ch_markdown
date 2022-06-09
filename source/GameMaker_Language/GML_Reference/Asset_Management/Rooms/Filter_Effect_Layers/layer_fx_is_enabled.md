# layer_fx_is_enabled

This function returns whether the filter/effect for a layer is enabled.
You specify either the ID or the name of the layer you want to target,
and the function returns a boolean value indicating whether the layer's
FX is enabled ( true ) or disabled ( false ).

#### Syntax:

``` gml
layer_fx_is_enabled(layer_name_or_id);
```

|                  |                                                                                                                                                                                                                  |                                      |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument         | Type                                                                                                                                                                                                             | Description                          |
| layer_name_or_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The name or ID of the layer to check |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
x = xstart;
y = ystart;
hp = hp_max;

if (layer_fx_is_enabled("DesaturateLayer"))
{
    layer_enable_fx("DesaturateLayer", false);
}
```

The above code "respawns" the instance, by moving it to its original
position and refilling its HP. It then checks if the Desaturate FX layer
is enabled, and if it is, disables it.
