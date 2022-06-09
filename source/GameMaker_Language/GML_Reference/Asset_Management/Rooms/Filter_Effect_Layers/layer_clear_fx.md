# layer_clear_fx

This function is used to clear the FX struct that is applied to the
specified layer. You specify either the ID or the name of the layer you
want to modify and this function will remove the FX struct that is
applied to that layer, disabling its effects completely. If you use this
function to temporarily disable an effect and need to restore it layer,
you should first save the FX struct for the layer by calling
[layer_get_fx()](layer_get_fx) and then call this function to clear
it on the layer. You can later apply it back to the layer by calling
[layer_set_fx()](layer_set_fx) , which will re-enable the effect.

#### Syntax:

``` gml
layer_clear_fx(layer_name_or_id);
```

|                  |                                                                                                                                                                                                                  |                                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Argument         | Type                                                                                                                                                                                                             | Description                                     |
| layer_name_or_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The name or ID of the layer to clear the FX for |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
// Disable effect
if (keyboard_check_pressed(ord("E")))
{
    if (layer_get_fx("EffectLayer") != -1)
    {
        temp_fx = layer_get_fx("EffectLayer");
        layer_clear_fx("EffectLayer");
    }
}
// Re-enable effect
else if (keyboard_check_pressed(ord("F")))
{
    if (temp_fx != -1)
    {
        layer_set_fx("EffectLayer", temp_fx);
        temp_fx = -1;
    }
}
```

The above code checks if the "E" key is pressed, and then checks if the
layer "EffectLayer" has a filter/effect applied to it; in that case it
stores its FX struct in a temporary instance variable and clears the
layer of any filters/effects. When the "F" key is pressed, it checks if
the temporary variable holds something other than -1, and in that case
it applies that FX back to the layer and resets the temporary variable
to -1. All of this essentially allows you to enable and disable an
effect whenever you need without losing its parameters.
