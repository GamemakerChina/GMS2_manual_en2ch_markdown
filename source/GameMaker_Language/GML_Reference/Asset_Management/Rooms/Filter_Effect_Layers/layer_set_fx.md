# layer_set_fx

This function is used to assign an FX struct to a Room Layer. You
specify either the ID or the name of the layer you want to modify, and
then an FX struct (as returned from [fx_create()](fx_create) or
[layer_get_fx()](layer_get_fx) ) which will be applied to the
specified layer, making the effect visible in the room. If you specify a
layer that is not a Filter/Effect Layer but is of another type (such as
an Instance Layer, Asset Layer, Tile Layer, etc.) then the effect will
be applied to the contents of that layer as well as to any layers below
it. Note that if the specified layer already has an FX struct assigned
to it, it will be replaced by the new one.

#### Syntax:

``` gml
layer_set_fx(layer_name_or_id, filter_or_effect);
```

|                  |                                                                                                                                                                                                                  |                                       |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| Argument         | Type                                                                                                                                                                                                             | Description                           |
| layer_name_or_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The name or ID of the layer to modify |
| filter_or_effect |  [FX Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Filter_Effect_Layers/fx_create)                                                                                       | The FX struct to apply to the layer   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _fx_tint = fx_create("_filter_tintfilter");
fx_set_parameter(_fx_tint, "g_TintCol", [1, 0, 0, 1]);
layer_set_fx("EffectLayer", _fx_tint);
```

The above code creates a new FX struct from the "\_filter_tintfilter"
effect, which is the "Colour Tint" filter found in the Room Editor. It
assigns a value to its "g_TintCol" parameter which is the colour of the
tint, and as it's a vec4 internally, it takes an array containing four
values (corresponding to its red, green, blue and alpha values). The FX
struct for the tint is then applied to an FX layer.
