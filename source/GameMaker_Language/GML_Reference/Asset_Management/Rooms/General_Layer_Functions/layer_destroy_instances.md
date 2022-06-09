# layer_destroy_instances

This function can be used to destroy all the instances assigned to the
given layer. You supply the layer ID (which you get when you create the
layer using [ layer_create() ](layer_create) ) or the layer name (as
a string - this will have a performance impact), and then all instances
that are on the layer will be removed from the game, triggering their
**Destroy** and **Clean Up** events.

#### Syntax:

``` gml
layer_destroy_instances(layer_id)
```

|          |                                                                                                                                                                                                                  |                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                      |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer (or the layer name as a string) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if global.game_over
{
    layer_destroy_instances(layer);
}
```

The above code will check a global variable and if it's true then all
instances that are on the layer of the calling instance will be
destroyed (including the calling instance).
