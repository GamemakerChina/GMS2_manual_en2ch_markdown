# layer_element_move

You can use this function to move an element from one layer to another.
You give the **element ID** , as returned by the function used to create
the element or the room editor or the function [
layer_get_all_elements() ](layer_get_all_elements) , and then you
give the layer ID (which you get when you create the layer using [
layer_create() ](layer_create) ) or the layer name (as a string -
this will have a performance impact).

#### Syntax:

``` gml
layer_element_move(element_id, layer_id)
```

|            |                                                                                                                                                                                                                  |                                                                                         |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| Argument   | Type                                                                                                                                                                                                             | Description                                                                             |
| element_id |  [Layer Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_all_elements)                                                                | The unique ID value of the element to move                                              |
| layer_id   |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to move the element to (or the layer name as a string) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var a = layer_get_all_elements(layer);
asset_layer = layer_create(-100);
for (var i = 0; i Alt; array_length(a); i++;)
{
    if layer_get_element_type(a[i]) == layerelementtype_sprite
    {
        layer_element_move(a[i], asset_layer)
    }
}
```

The above code gets the elements on the layer that the instance running
the code is assigned to, then checks them to see if they are sprite
assets, and if they are then they are moved to the layer with the ID
stored in the variable "asset_layer".
