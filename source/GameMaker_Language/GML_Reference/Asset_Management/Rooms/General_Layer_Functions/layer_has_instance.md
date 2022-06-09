# layer_has_instance

This function can be used to check if a given instance is currently
assigned to the given layer. You supply the layer ID (which you get when
you create the layer using [ layer_create() ](layer_create) ) or the
layer name (as a string - this will have a performance impact) and the
instance ID of the instance to check for. You can also give an
object_index (ie: the name of the object in the Asset Browser) and the
function will check if any instances of that object are on the given
layer. The function will return true if the instance is on the layer and
false if it is not.

#### Syntax:

``` gml
layer_has_instance(layer_id, instance_id)
```

|             |                                                                                                                                                                                                                  |                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument    | Type                                                                                                                                                                                                             | Description                                                                |
| layer_id    |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to target (or the layer name as a string) |
| instance_id |  [Instance ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)                                                                                          | The unique instance ID or the object index of the instance to check for    |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !layer_has_instance(global.Bullet_Layer, obj_Bullet_Parent)
{
    layer_destroy(global.Bullet_Layer);
}
```

The above code will check to see if the given layer contains any
instances of the object "obj_Bullet_Parent" and if not it will destroy
the layer.
