# layer_sprite_get_id

This function can be used to retrieve the unique ID value of a sprite
element on a layer. You supply the layer ID (which you get when you
create the layer using [ layer_create()
](../General_Layer_Functions/layer_create) or when you use the layer
name along with [ layer_get_id()
](../General_Layer_Functions/layer_get_id) ) and the name of the
sprite element as defined in the Room Editor. The function will return
the ID value associated with that sprite element on the layer. Note that
this function is specifically designed for use with sprites that have
been added in the IDE on an asset layer, and if you added a sprite to a
layer through code using the function [ layer_sprite_create()
](layer_sprite_create) , then the ID returned by that function
should be used for all future reference (as that sprite element will
have no name to be passed into this function). If the specified layer
does not exist, or the given sprite element cannot be found, the
function will return -1.

#### Syntax:

``` gml
layer_sprite_get_id(layer_id, sprite_element_name)
```

|                     |                                                                                                                                                                                                                  |                                                                                  |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Argument            | Type                                                                                                                                                                                                             | Description                                                                      |
| layer_id            |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to target                                       |
| sprite_element_name |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                      | The unique name of the sprite element on the layer as defined in the Room Editor |

#### Returns:

``` gml
 Sprite Element ID
```

#### Example:

``` gml
var lay_id = layer_get_id("Assets_trees");
var back_id = layer_sprite_get_id(lay_id, "graphic_254367CB");
layer_sprite_change(back_id, spr_Trees_Winter);
```

The above code will get the layer ID for the layer named "Assets_trees"
and then use that to retrieve the ID of the sprite element
"graphic_254367CB" on that layer. The retrieved sprite element ID is
then used to change the element's sprite.
