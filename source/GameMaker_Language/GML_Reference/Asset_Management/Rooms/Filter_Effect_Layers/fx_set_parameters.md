# fx_set_parameters

This function is used to change the parameters of a filter/effect. You
specify an FX struct (as returned from [fx_create()](fx_create) or
[layer_get_fx()](layer_get_fx) ) and a struct containing its
parameters (as returned from
[fx_get_parameters()](fx_get_parameters) ). This will make your
changes visible in the layer that the FX struct is assigned to. Your
parameter struct is not required to contain every parameter that is
applicable to the filter/effect, and only the variables that are present
in the given struct will be updated for the filter/effect.

#### Syntax:

``` gml
fx_set_parameters(filter_or_effect, parameter_struct);
```

|                  |                                                                                                                             |                                                          |
|------------------|-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| Argument         | Type                                                                                                                        | Description                                              |
| filter_or_effect |  [FX Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Filter_Effect_Layers/fx_create)  | The FX struct to modify                                  |
| parameter_struct |  [Struct](../../../../../../GameMaker_Language/GML_Overview/Structs)                                                    | A struct containing the parameters for the filter/effect |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _fx_struct = layer_get_fx("TintEffect");

if (_fx_struct != -1)
{
    var _params = fx_get_parameters(_fx_struct);
    var _osc = sin(current_time / 1000);
    _params.g_TintCol = [_osc, 0.3 + _osc, 0.6 + _osc, 1];

    fx_set_parameters(_fx_struct, _params);
}
```

The above code gets the FX struct for a layer that is assumed to have
the "Colour Tint" filter applied to it, and retrieves its parameter
struct by calling [ fx_get_parameters() ](fx_get_parameters) . After
that it creates an oscillating value by using
[sin()](../../../Maths_And_Numbers/Angles_And_Distance/sin) and
[current_time](../../../Maths_And_Numbers/Date_And_Time/current_time)
, which is then used for the RGBA values for the tint effect so it keeps
animating. The RGBA array is assigned to the g_TintCol variable in the
parameter struct, and the struct is then applied back to the FX struct
by calling fx_set_parameters() .
