# layer_get_visible

With this function you can check whether a layer is visible or not. You
supply the layer ID (which you get when you create the layer using [
layer_create() ](layer_create) ) or the layer name (as a string -
this will have a performance impact) and the function will return true
if it is visible, and false otherwise.

#### Syntax:

``` gml
layer_get_visible(layer_id)
```

|          |                                                                                                                                                                                                                  |                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                                |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to target (or the layer name as a string) |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var lay_id = layer_get_id("Instances");
if layer_get_visible(lay_id)
{
    layer_set_visible(lay_id, false);
}
else
{
    layer_set_visible(lay_id, true);
}
```

The above code gets the ID value for the layer named "Instances" in the
room editor, then uses the ID to check if the layer is visible or not,
toggling the layer visibility depending on the returned value.
