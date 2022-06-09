# fx_get_parameter

This function is used to retrieve the value of a parameter from an FX
Struct. You specify the FX struct to read (as returned from
[fx_create()](fx_create) or [layer_get_fx()](layer_get_fx) )
and the name of the parameter as a string, and the function returns its
current value. This may be a real value, or an array if the parameter is
a vector (which is a group of values, such as a vec4 which stores an
RGBA colour). Find the parameter names for a filter/effect on this page:
[FX Types &
Parameters](../../../../../The_Asset_Editors/Room_Properties/FX/All_Filter_Effect_Types)
.

#### Syntax:

``` gml
fx_get_parameter(filter_or_effect, parameter_name);
```

|                  |                                                                                                                             |                                                             |
|------------------|-----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Argument         | Type                                                                                                                        | Description                                                 |
| filter_or_effect |  [FX Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Filter_Effect_Layers/fx_create)  | The FX struct to get the parameter from                     |
| parameter_name   |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                 | The name of the parameter to get the value of (as a string) |

#### Returns:

``` gml
 Real

or

 Array
```

#### Example:

``` gml
var _fx_struct = layer_get_fx("TintEffect");
var _tint_colour = fx_get_parameter(_fx_struct, "g_TintCol");
show_debug_message("The currently active tint colour is: " + string(_tint_colour));
```

The above code retrieves the FX struct from a layer that is assumed to
have the "Colour Tint" filter applied to it, and gets the value of its
"g_TintCol" parameter, which returns an array containing the 4 values
for its tint colour (red, green, blue and alpha). It then prints that
value to the output log.
