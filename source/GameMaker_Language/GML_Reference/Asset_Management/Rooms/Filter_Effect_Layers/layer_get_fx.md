# layer_get_fx

This function is used to retrieve the FX struct for a layer. You specify
either the ID or the name of the layer you want to target and the
function will return a struct containing information on its applied
effect. This struct will be similar to the struct you get from
[fx_create()](fx_create) , and the functions [ fx_get_parameter
](fx_get_parameter) / [ s ](fx_get_parameters) and
[fx_set_parameter](fx_set_parameter) / [s](fx_set_parameters)
can be used on it to read and modify its parameters. If the specified
layer has no filters/effects applied to it, the function will return -1.

#### Syntax:

``` gml
layer_get_fx(layer_name_or_id);
```

|                  |                                                                                                                                                                                                                  |                                     |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Argument         | Type                                                                                                                                                                                                             | Description                         |
| layer_name_or_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The name or ID of the layer to read |

#### Returns:

``` gml
 FX Struct

(or -1 if not found)
```

#### Example:

``` gml
var layers = layer_get_all();
for(var i = 0; i &amp;lt; array_length(layers); i ++)
{    
    var layer_fx = layer_get_fx(layers[i]);
    
    if (layer_fx != -1)
    {
        if (fx_get_name(layer_fx) == "_filter_tintfilter")
        {            
            fx_set_parameter(_fx_tint, "g_TintCol", [0, 0, 1, 1]);
        }
    }
}
```

The above code runs a
[for](../../../../GML_Overview/Language_Features/for) loop through
all the layers present in the room, and checks each layer for an FX
struct. If a layer has an FX struct, it checks the name of that
filter/effect by calling [ fx_get_name() ](fx_get_name) on it; if
it's equal to "\_filter_tintfilter" meaning that it's a "Colour Tint"
filter, it changes its tint colour to blue.
