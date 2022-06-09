# fx_get_parameters

This function is used to retrieve a
[struct](../../../../GML_Overview/Structs) containing all the
parameters for the given FX struct. You specify an FX struct (as
returned from [fx_create()](fx_create) or
[layer_get_fx()](layer_get_fx) ) and this function returns a struct
containing variables for all parameters applicable to that
filter/effect. Parameters that use vectors (i.e. groups of values) will
be present as arrays. You can get the names of all parameters in a
separate array by calling
[fx_get_parameter_names()](fx_get_parameter_names) , or find them on
this page: [FX Types &
Parameters](../../../../../The_Asset_Editors/Room_Properties/FX/All_Filter_Effect_Types)
. Changing values in this struct will not apply those changes to the
filter/effect; you will need to call
[fx_set_parameters()](fx_set_parameters) to apply the modified
struct back to the filter/effect for any changes to take effect.

#### Syntax:

``` gml
fx_get_parameters(filter_or_effect);
```

|                  |                                                                                                                             |                                                         |
|------------------|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Argument         | Type                                                                                                                        | Description                                             |
| filter_or_effect |  [FX Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Filter_Effect_Layers/fx_create)  | The FX struct for which the parameters will be returned |

#### Returns:

``` gml
 Struct

(or -1 on failure)
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
struct by calling fx_get_parameters() . After that it creates an
oscillating value by using
[sin()](../../../Maths_And_Numbers/Angles_And_Distance/sin) and
[current_time](../../../Maths_And_Numbers/Date_And_Time/current_time)
, which is then used for the RGBA values for the tint effect so it keeps
animating. The RGBA array is assigned to the g_TintCol variable in the
parameter struct, and the struct is then applied back to the FX struct
by calling [ fx_set_parameters() ](fx_set_parameter) .
