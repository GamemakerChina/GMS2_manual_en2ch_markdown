# tilemap_tileset

Using this function you can change the tile set asset assigned to a
given tile map element on a layer. You give the tile map element ID
(which you get when you create a tile map element using [
layer_tilemap_create() ](layer_tilemap_create) or when you use the
function [ layer_tilemap_get_id() ](layer_tilemap_get_id) ), and
then supply a tile set index and the tile map will be given the new
sprite.

#### Syntax:

``` gml
tilemap_tileset(tilemap_element_id, tileset_index)
```

|                    |                                                                                                                                             |                                                       |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                           |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tile map element to change |
| tileset_index      |  [Tile Set Asset](../../../../../../The_Asset_Editors/Tile_Sets)                                                                        | The new tile set index to use                         |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_trees");
var tile_id = layer_tilemap_get_id(lay_id);
if tilemap_get_tileset(tile_id) != ts_Nighttime
{
    tilemap_tileset(tile_id, ts_Nighttime);
}
```

The above code checks the current tile set assigned to the tile map on
the layer "Tiles_trees" and if it is not "ts_Nighttime" then that tile
set is assigned to the tile map.
