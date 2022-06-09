# layer_destroy

This function will destroy the given layer. You supply the layer ID
(which you get when you create the layer using [ layer_create()
](layer_create) ) or the layer name (as a string - this will have a
performance impact) and this will remove it from the current room. If
the layer is one that has been designed in the room editor, then the
next time you leave the room and then return, the layer will be
recreated again with the original contents, however if the room is
persistent, the layer will be removed unless room persistence is
switched off again. When you destroy a layer in this way, all it's
contents will be removed too, so any reference IDs for backgrounds or
tile maps, etc... will no longer be valid and any instances assigned to
the layer will be destroyed (performing their **Destroy Event** at the
same time, if they have one, as well as the **Clean Up Event** ).

#### Syntax:

``` gml
layer_destroy(layer_id)
```

|          |                                                                                                                                                                                                                  |                                                                             |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                                 |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to destroy (or the layer name as a string) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if !instance_exists(obj_Bullet_Parent)
{
    layer_destroy(global.Bullet_Layer);
}
```

The above code will check to see if any instances of the object
"obj_Bullet_Parent" exists, and if they don't it will destroy the layer
with the ID stored in the global variable.
