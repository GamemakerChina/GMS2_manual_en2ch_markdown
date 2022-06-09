# layer_sprite_create

With this function you can assign a sprite resource to a layer to be
used in your project. You supply the layer ID (which you get when you
create the layer using [ layer_create()
](../General_Layer_Functions/layer_create) or when you use the layer
name along with [ layer_get_id()
](../General_Layer_Functions/layer_get_id) ), a position within the
room, and a sprite index (which would be the name of the sprite as shown
in the Asset Browser), and it will be added to the layer. The function
returns the unique ID value for the element, which can then be used in
further layer functions for sprites.

#### Syntax:

``` gml
layer_sprite_create(layer_id, x, y, sprite)
```

|          |                                                                                                                                                                                                                  |                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to target |
| x        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                        | The x position to use                      |
| y        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                        | The y position to use                      |
| sprite   |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)                                                                                                                                                 | The sprite index to be used                |

#### Returns:

``` gml
 Sprite Element ID
```

#### Example:

``` gml
global.asset_layer = layer_create(10000);
for (var i = 0; i&amp;lt; 10; i++;)
{
    var _x = random(room_width);
    var _y = room_height - 100;
    global.asset_spr_trees[i] = layer_sprite_create(global.asset_layer, _x, _y, spr_Trees);
}
```

The above code creates a new layer and then adds 10 new sprite elements
to it, storing the ID of each element to an array.
