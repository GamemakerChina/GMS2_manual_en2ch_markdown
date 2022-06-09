# layer_add_instance

This function can be used to move a given instance from the layer it is
currently on to another layer. You supply the layer ID (which you get
when you create the layer using [ layer_create() ](layer_create) )
or the layer name (as a string - this will have a performance impact)
and the instance ID of the instance to move between layers. For example,
say your player is on a layer that is at a lower depth than another
layer and you want it to appear behind the layers between the two. You
can use this function to switch the player from the foreground layer to
the background layer and make it appear behind the other layers being
drawn. ** NOTE ** This function cannot be used to add a new instance to
a layer. You **must** have created the instance previously and stored
its ID to a variable. **NOTE** : This function is only valid within the
scope of the current room and cannot be used when the scope has been
changes using the function
[layer_set_target_room()](layer_set_target_room) .

#### Syntax:

``` gml
layer_add_instance(layer_id, instance_id)
```

|             |                                                                                                                                                                                                                  |                                                                                     |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| Argument    | Type                                                                                                                                                                                                             | Description                                                                         |
| layer_id    |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the instance layer to target (or the layer name as a string) |
| instance_id |  [Instance ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)                                                                                          | The unique instance ID value of the instance to move over to the target layer       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var near = instance_nearest(x, y, obj_Tree);
var layer_id = layer_get_id("Instances Front");
layer_add_instance(layer_id, near);
```

The above code will first get the index of the nearest instance to the
given x/y position and store it in a local variable. It then gets the
unique instance layer ID for the layer named "Instances Front", and
moves the found instance onto that layer.
