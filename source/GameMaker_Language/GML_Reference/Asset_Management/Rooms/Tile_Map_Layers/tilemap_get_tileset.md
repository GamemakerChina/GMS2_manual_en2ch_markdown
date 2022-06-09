# tilemap_get_tileset

Using this function you can retrieve the index value of the Tile Set
asset assigned to a given tile map element on a layer. You give the Tile
Map element ID (which you get when you create a tile map element using [
layer_tilemap_create() ](layer_tilemap_create) or when you use the
function [ layer_tilemap_get_id() ](layer_tilemap_get_id) ), and the
function will return the Tile Set asset index.

#### Syntax:

``` gml
tilemap_get_tileset(tilemap_element_id);
```

|                    |                                                                                                                                             |                                                                      |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                                          |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the Tile Map element to get the tile set from |

#### Returns:

``` gml
 Tile Set Asset
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_trees");
var map_id = layer_tilemap_get_id(lay_id);
if tilemap_get_tileset(map_id) != ts_Nighttime
{
    tilemap_tileset(map_id, ts_Nighttime);
}
```

The above code checks the current tile set assigned to the layer
"Tiles_trees" and if it is not "ts_Nighttime" then that tile set is
assigned to the tile map.
