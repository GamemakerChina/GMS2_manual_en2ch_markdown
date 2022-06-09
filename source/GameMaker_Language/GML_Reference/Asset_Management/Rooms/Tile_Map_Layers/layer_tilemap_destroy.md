# layer_tilemap_destroy

This function will destroy the given tile map element. You supply the
tile map ID (which you get when you create the tile map using [
layer_tilemap_create() ](layer_tilemap_create) or when you use the
layer ID along with [ layer_get_tilemap_id() ](layer_tilemap_get_id)
) and this will remove it. Note that this does *not* remove the layer,
only the tile map from it, and if the tile map is one that has been
added in the room editor, then the next time you leave the room and then
return, the tile map will be recreated again. However if the room is
persistent, the tile map will be removed unless room persistence is
switched off again.

#### Syntax:

``` gml
layer_tilemap_destroy(tilemap_element_id)
```

|                    |                                                                                                                                             |                                                     |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                         |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tile map to be destroyed |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_trees");
var tile_id = layer_tilemap_get_id(lay_id);
if layer_tilemap_exists(lay_id, tile_id)
{
    layer_tilemap_destroy(tile_id);
}
```

The above code checks the layer "Tiles_trees" to see if the given tile
map element exists and if it does, then it is destroyed (but not the
layer).
