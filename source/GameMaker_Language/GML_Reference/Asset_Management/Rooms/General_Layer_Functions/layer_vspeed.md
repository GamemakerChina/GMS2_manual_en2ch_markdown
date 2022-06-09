# layer_vspeed

You can use this function to set the vertical speed (in pixels per game
frame) of the layer within the currently scoped room. You supply the
layer ID (which you get when you create the layer using [ layer_create()
](layer_create) ) or the layer name (as a string - this will have a
performance impact) and the speed value to set, where a positive value
is downwards and a negative value upwards.

#### Syntax:

``` gml
layer_vspeed(layer_id, vspd)
```

|          |                                                                                                                                                                                                                  |                                                               |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                   |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to set the vertical speed of |
| vspd     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                        | The vertical speed (in pixels per game frame) to set          |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Sprites");
if layer_get_hspeed(lay_id) != 0 || layer_get_vspeed(lay_id) != 0
{
    layer_hspeed(lay_id, 0);
    layer_vspeed(lay_id, 0);
}
```

The above code checks the given layer horizontal and vertical speeds and
if they are not both set to 0 then it is sets them to 0.
