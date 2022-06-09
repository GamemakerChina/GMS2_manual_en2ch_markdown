# layer_set_visible

With this function you can toggle the visibility of a layer. You supply
the layer ID (which you get when you create the layer using [
layer_create() ](layer_create) ) or the layer name (as a string -
this will have a performance impact) as well as the toggle value for the
layer where visible is true and invisible is false . When a layer is
invisible, nothing that is assigned to the layer will be drawn, and if
any instances are assigned to the layer then they will not even run
their draw event (much the same as if you set the instance variable
visible to false ). Note that any instances that are already flagged as
invisible will *not* be flagged as visible if the layer they are on is
set to visible, as these are two independent settings, although their
behaviour is the same.

#### Syntax:

``` gml
layer_set_visible(layer_id, visible)
```

|          |                                                                                                                                                                                                                  |                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                                |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to target (or the layer name as a string) |
| visible  |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                     | Whether the layer should be visible ( true ) or not ( false )              |

#### Returns:

``` gml
N/A
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
