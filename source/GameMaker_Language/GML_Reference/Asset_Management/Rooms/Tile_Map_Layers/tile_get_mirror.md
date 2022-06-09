# tile_get_mirror

This function can be used to check whether in a given set of tile-data
the tile has been mirrored or not. You give the tile-data, which can be
retrieved using the function [ tilemap_get() ](tilemap_get) , and
the function will return true if the tile is mirrored, or false if not.

#### Syntax:

``` gml
tile_get_mirror(tiledata)
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
var mx = tilemap_get_cell_x_at_pixel(map_id, mouse_x, mouse_y);
var my = tilemap_get_cell_y_at_pixel(map_id, mouse_x, mouse_y);
var data = tilemap_get(map_id, mx, my);
var bool = !tile_get_mirror(data);
data = tile_set_mirror(data, bool);
tilemap_set(map_id, data, mx, my);
```

The above code gets the tile map ID from the given layer and then gets
the x and y cell position for the tile under the mouse. This position is
then used to get the tile-data which is mirrored and then used to set
the tile again.
