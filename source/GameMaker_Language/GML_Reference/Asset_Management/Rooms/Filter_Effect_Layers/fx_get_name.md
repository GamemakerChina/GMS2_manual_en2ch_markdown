# fx_get_name

This function is used to retrieve the name of a filter/effect from its
struct. You specify the FX struct to read (as returned from
[fx_create()](fx_create) or [layer_get_fx()](layer_get_fx) )
and the function returns its name as a string. This name can then be
passed into [fx_create()](fx_create) to create a new FX struct
using the same filter/effect type.

#### Syntax:

``` gml
fx_get_name(filter_or_effect);
```

|                  |                                                                                                                             |                                  |
|------------------|-----------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| Argument         | Type                                                                                                                        | Description                      |
| filter_or_effect |  [FX Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Filter_Effect_Layers/fx_create)  | The FX struct to get the name of |

#### Returns:

``` gml
 String
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
filter/effect by calling fx_get_name() on it; if it's equal to
"\_filter_tintfilter" meaning that it's a "Colour Tint" filter, it
changes its tint colour to blue.
