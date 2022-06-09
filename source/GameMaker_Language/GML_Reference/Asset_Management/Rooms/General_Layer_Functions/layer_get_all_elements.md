# layer_get_all_elements

You can use this function to get the *element IDs* of the given layer.
You supply the layer ID (which you get when you create the layer using [
layer_create() ](layer_create) ) or the layer name (as a string -
this will have a performance impact) and the function will return an
[array](../../../../GML_Overview/Arrays) of IDs, where each entry in
the array is a unique ID for an element on that layer. For example, if
the layer is an Asset Layer, the array will be populated with the ID
values for each sprite asset that is assigned to the layer. Note that
using code to work with layers means that you can assign different
element types to the same layer - so you can have sprite assets along
with instances, for example - in which case you can then use the
function [ layer_get_element_type() ](layer_get_element_type) to get
the type of element the ID relates to.

#### Syntax:

``` gml
layer_get_all_elements(layer_id)
```

|          |                                                                                                                                                                                                                  |                                                                                           |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                                               |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to get the elements from (or the layer name as a string) |

#### Returns:

``` gml
 Array

of

 Layer Element ID

s
```

#### Example:

``` gml
var a = layer_get_all_elements(layer);
for (var i = 0; i &amp;lt; array_length(a); i++;)
{
    if layer_get_element_type(a[i]) == layerelementtype_sprite
    {
        layer_sprite_destroy(a[i])
    }
}
```

The above code gets the IDs for all the instance elements assigned to
the layer of the instance running the code. The code then checks to see
if any of the returned elements are sprite assets and if they then they
are destroyed.
