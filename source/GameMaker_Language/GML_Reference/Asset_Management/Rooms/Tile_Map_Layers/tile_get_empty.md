# tile_get_empty

This function can be used to check whether a given set of tile-data is
for an empty tile or not. You give the tile-data, which can be retrieved
using the function [ tilemap_get() ](tilemap_get) , and the function
will return true if the tile is empty, or false if there is a tile
index.

#### Syntax:

``` gml
tile_get_empty(tiledata)
```

|          |                                                                                                                          |                        |
|----------|--------------------------------------------------------------------------------------------------------------------------|------------------------|
| Argument | Type                                                                                                                     | Description            |
| tiledata |  [Tile Data](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get)  | the tile-data to check |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_sky");
var map_id = layer_tilemap_get_id(lay_id);
for (var i = 0; i &amp;lt; tilemap_get_width(map_id); i++;)
{
    for (var j = 0; j &amp;lt; tilemap_get_height(map_id); j++;)
    {
        var data = tilemap_get(map_id, i, j);
        if !tile_get_empty(data)
        {
            data = tile_set_empty(data)
            tilemap_set(map_id, data, i, j);
        }
    }
}
```

The above code gets the tile map ID from the given layer and then
proceeds to check every tile cell on the map to see if it has data or
not. If it does, the tile is set to empty.
