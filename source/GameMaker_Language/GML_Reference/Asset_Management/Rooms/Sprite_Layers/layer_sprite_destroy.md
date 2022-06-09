# layer_sprite_destroy

This function will destroy the given sprite element. You supply the
sprite ID (which you get when you create the sprite using [
layer_sprite_create() ](layer_sprite_create) or when you use the
layer ID along with [ layer_get_sprite_id() ](layer_sprite_get_id) )
and this will remove it. Note that this does *not* remove the layer,
only the sprite from it, and if the sprite is one that has been added in
the room editor, then the next time you leave the room and then return,
the sprite will be recreated again. However if the room is persistent,
the sprite will be removed unless room persistence is switched off
again.

#### Syntax:

``` gml
layer_sprite_destroy(sprite_element_id)
```

|                   |                                                                                                                                        |                                                   |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| Argument          | Type                                                                                                                                   | Description                                       |
| sprite_element_id |  [Sprite Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sprite_Layers/layer_sprite_get_id)  | The unique ID value of the sprite to be destroyed |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Asset_Trees");
if layer_sprite_exists(lay_id, global.Asset_spr_trees)
{
    layer_sprite_destroy(lay_id);
}
```

The above code checks the layer "Asset_Trees" to see if the given sprite
element exists and if it does, then it is destroyed (but not the layer).
