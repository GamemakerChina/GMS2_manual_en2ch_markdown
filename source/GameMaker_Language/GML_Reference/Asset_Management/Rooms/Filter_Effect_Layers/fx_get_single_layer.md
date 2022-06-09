# fx_get_single_layer

This function returns whether the supplied filter/effect is using Single
Layer mode ( true ) or not ( false ). See [ fx_set_single_layer()
](fx_set_single_layer) for information on Single Layer mode. You
specify an FX struct (as returned from [fx_create()](fx_create) or
[layer_get_fx()](layer_get_fx) ) and the function returns a boolean
that tells whether Single Layer mode is enabled or not for the FX.

#### Syntax:

``` gml
fx_get_single_layer(filter_or_effect);
```

|                  |                                                                                                                             |                       |
|------------------|-----------------------------------------------------------------------------------------------------------------------------|-----------------------|
| Argument         | Type                                                                                                                        | Description           |
| filter_or_effect |  [FX Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Filter_Effect_Layers/fx_create)  | The FX struct to read |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var _fx = layer_get_fx("Distort");

if (!fx_get_single_layer(_fx))
{
    fx_set_single_layer(_fx, true);
}
```

The above code gets the FX struct from a layer called "Distort" and
checks if Single Layer mode is enabled on it. If it isn't, it enables
Single Layer mode for that FX.
