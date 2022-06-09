# fx_set_single_layer

This function is used to enable or disable "Single Layer" mode for a
filter/effect. By default, a filter/effect is applied to the layer that
it is [assigned to](layer_set_fx) and all layers below that layer,
however you can enable Single Layer mode on an FX struct to make sure
that it's only applied to the layer that it is assigned to. You
specify an FX struct (as returned from [fx_create()](fx_create) or
[layer_get_fx()](layer_get_fx) ) and a boolean value to enable (
true ) or disable ( false ) Single Layer mode. The following visual
shows a filter being used with Single Layer mode disabled (which is the
default behaviour for all FX layers) and the same filter with Single
Layer mode enabled:

![Single Layer Mode
OFF](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Rooms/FX_single_layer_off.png)

![Single Layer Mode
ON](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Rooms/FX_single_layer_on.png)

NOTE When you enable Single Layer mode for an FX, make sure that you
apply it to a layer that is not an [FX
layer](../../../../../The_Asset_Editors/Room_Properties/Filters_and_Effects)
, because an FX layer by itself contains nothing and so no filter/effect
will be visible.

#### Syntax:

``` gml
fx_set_single_layer(filter_or_effect, enable);
```

|                  |                                                                                                                             |                                                                               |
|------------------|-----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| Argument         | Type                                                                                                                        | Description                                                                   |
| filter_or_effect |  [FX Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Filter_Effect_Layers/fx_create)  | The FX struct to modify                                                       |
| enable           |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                | A boolean value to enable ( true ) or disable ( false ) Single Layer Mode     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
shake_fx = fx_create("_filter_screenshake");
fx_set_single_layer(shake_fx, true);
layer_set_fx("ShakeyThings", shake_fx);
```

The above code creates a new screenshake FX, enables Single Layer mode
on it and then applies it to a room layer. This means that the
screenshake filter will only be applied to the "ShakeyThings" layer.
