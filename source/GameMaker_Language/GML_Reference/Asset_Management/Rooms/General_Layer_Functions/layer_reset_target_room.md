# layer_reset_target_room

This function is used to reset the layer target to the current room. See
the function [ layer_set_target_room() ](layer_set_target_room) for
further information.

#### Syntax:

``` gml
layer_reset_target_room()
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
layer_set_target_room(rm_Game);
var l = layer_get_id("SpriteAssets");
repeat(50)
{
    layer_sprite_create(l, irandom(1000), irandom(1000), spr_Trees);
}
layer_reset_target_room();
```

The above code sets the target room to the room "rm_Game" and then gets
the layer ID for the layer called "SpriteAssets" in that room. This
layer ID is then used to add 50 random sprite assets to the layer,
before the layer target is reset to the current room.
