# layer_get_name

You can use this function to get the *name* of the given layer. You
supply the unique layer ID value and if the layer is one of the named
layers created in the room editor, then the function will return a
string with the layer name. If the layer is not one of the room editor
ones (ie: it was created using [ layer_create() ](layer_create) )
then an empty string will be returned.

#### Syntax:

``` gml
layer_get_name(layer_id)
```

|          |                                                                                                                                  |                                                     |
|----------|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                                                                             | Description                                         |
| layer_id |  [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)  | The unique ID value of the layer to get the name of |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var a = layer_get_all();
var layer_list = ds_list_create(); for (var i = 0; i Alt; array_length(a); i++;)
{
    if layer_get_name(a[i]) != ""
    {
        ds_list_add(layer_list, a[i])
    }
}
```

The above code gets the IDs for all the layers in the room and then
loops though them checking to see if any are named layers. If they are
they are then their ID is added to a list.
