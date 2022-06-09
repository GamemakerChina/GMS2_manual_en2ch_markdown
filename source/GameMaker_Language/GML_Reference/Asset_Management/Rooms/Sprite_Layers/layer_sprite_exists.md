# layer_sprite_exists

You can use this function to check and see if a sprite element exists on
any given layer. You supply the layer ID (which you get when you create
the layer using [ layer_create()
](../General_Layer_Functions/layer_create) ) or the layer name (as a
string - this will have a performance impact) and the sprite element ID
(which you get when you create a sprite element using [
layer_sprite_create() ](layer_sprite_create) or when you use the
function [ layer_sprite_get_id() ](layer_sprite_get_id) ) and the
function will return either true if the element exists, or false if it
does not. **NOTE** : This function works within the scope of the current
target room - by default the room in which the function is called -
which can be set using the function [ layer_set_target_room()
](../General_Layer_Functions/layer_set_target_room) .

#### Syntax:

``` gml
layer_sprite_exists(layer_id, sprite_element_id)
```

|                   |                                                                                                                                                                                                                  |                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument          | Type                                                                                                                                                                                                             | Description                                                                |
| layer_id          |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to target (or the layer name as a string) |
| sprite_element_id |  [Sprite Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sprite_Layers/layer_sprite_get_id)                                                                            | The unique ID value of the sprite element to check                         |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var lay_id = layer_get_id("Asset_Trees");
if layer_sprite_exists(lay_id, global.TreesSprites)
{
    layer_sprite_destroy(lay_id, global.TreesSprites);
}
```

The above code checks the layer "Asset_trees" to see if the given sprite
element exists and if it does, then it is destroyed (but not the layer).
