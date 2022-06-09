# layer_set_target_room

When you call this function you are telling GameMaker that *all further
layer functions should be applied to the given room* . In this way you
can procedurally change or generate layers and layer contents in a room
that is not the current room. When you are finished adding layers or
layer elements to a room, call the function [ layer_reset_target_room()
](layer_reset_target_room) to reset the room target (or call this
function again with a room argument of -1). Note that this function can
only be used on *rooms other than the current room* , and is designed so
that you can add/remove layers and layer elements to rooms other than
the room that is currently running. **WARNING!** While targeting another
room, you can use all the regular layer functions **except** you cannot
create instances using [ instance_create_layer()
](../../Instances/instance_create_layer) or [
instance_create_depth() ](../../Instances/instance_create_depth) ,
nor will the layer function [ layer_add_instance()
](layer_add_instance) be available.

#### Syntax:

``` gml
layer_set_target_room(room)
```

|          |                                                               |                                                    |
|----------|---------------------------------------------------------------|----------------------------------------------------|
| Argument | Type                                                          | Description                                        |
| room     |  [Room Asset](../../../../../../The_Asset_Editors/Rooms)  | The room to target for all further layer functions |

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
    var _x = irandom(1000);
    var _y = irandom(1000);
    layer_sprite_create(l, _x, _y, spr_Trees);
}
layer_reset_target_room();
```

The above code sets the target room to the room "rm_Game" and then gets
the layer ID for the layer called "SpriteAssets" in that room. This
layer ID is then used to add 50 random sprite assets to the layer,
before the layer target is reset to the current room.
