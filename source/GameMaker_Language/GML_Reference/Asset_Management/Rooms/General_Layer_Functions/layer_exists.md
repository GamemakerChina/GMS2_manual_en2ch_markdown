# layer_exists

This function can be used to check if the given **layer** exists. You
supply the layer ID (which you get when you create the layer using [
layer_create() ](layer_create) ) or the layer name (as a string -
this will have a performance impact) and the function will return a
*boolean* value of true if it exists or false if it does not. **NOTE** :
This function works within the scope of the current target room - by
default the room in which the function is called - which can be set
using the function [ layer_set_target_room()
](layer_set_target_room) .

#### Syntax:

``` gml
layer_exists(layer_name)
```

|            |                                                                                                                                                                                                                  |                                              |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument   | Type                                                                                                                                                                                                             | Description                                  |
| layer_name |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The name of the layer (a string or ID value) |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !layer_exists(global.tileLayer)
{
    global.tileLayer = layer_create(1000);
}
```

The above code will check to see if the layer stored in the global
variable actually exists, and if it does not then it is created.
