# fx_get_parameter_names

This function is used to retrieve the names of all parameters present in
a filter/effect. You specify the FX struct to read (as returned from
[fx_create()](fx_create) or [layer_get_fx()](layer_get_fx) )
and the function returns an array containing the names of the filter's
parameters as strings.

#### Syntax:

``` gml
fx_get_parameter_names(filter_or_effect);
```

|                  |                                                                                                                             |                                             |
|------------------|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| Argument         | Type                                                                                                                        | Description                                 |
| filter_or_effect |  [FX Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Filter_Effect_Layers/fx_create)  | The FX struct to get the parameter names of |

#### Returns:

``` gml
 Array

(of Strings)
```

#### Example:

``` gml
var _fx_struct = layer_get_fx("EffectLayer");
var _param_names = fx_get_parameter_names(_fx_struct);

for (var i = 0; i &amp;lt; array_length(_param_names); i ++) {
    show_debug_message("Parameter " + string(i) + ": " + _param_names[i]);
}
```

The above code retrieves the FX struct for a layer and gets its
parameter names in an array. It then runs a
[for](../../../../GML_Overview/Language_Features/for) loop on that
array and prints each parameter to the output log.
