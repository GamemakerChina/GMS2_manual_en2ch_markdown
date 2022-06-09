# tile_set_flip

This function can be used to set a given set of tile-data to flip the
tile or not. You give the tile-data, which can be retrieved using the
function [ tilemap_get() ](tilemap_get) , and then set the flip
argument to either true if you want the tile flipped, or false if you
want the tile to be in its default, un-flipped state. The function will
return a modified tile-data set which can then be applied using the [
tilemap_set() ](tilemap_set) function.

#### Syntax:

``` gml
tile_set_flip(tiledata, flip)
```

|          |                                                                                                                          |                                                     |
|----------|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                                                                     | Description                                         |
| tiledata |  [Tile Data](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get)  | the tile-data to set                                |
| flip     |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                             | Set to true to flip and false to leave it as-is     |

#### Returns:

``` gml
 Tile Data
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_sky"); var map_id = layer_tilemap_get_id(lay_id); var mx = tilemap_get_cell_x_at_pixel(map_id, mouse_x, mouse_y); var my = tilemap_get_cell_y_at_pixel(map_id, mouse_x, mouse_y); var data
= tilemap_get(map_id, mx, my); var bool = !tile_get_flip(data); data = tile_set_flip(data, bool); tilemap_set(map_id, data, mx, my);
```

The above code gets the tile map ID from the given layer and then gets
the x and y cell position for the tile under the mouse. This position is
then used to get the tile-data which is flipped and then used to set the
tile again.
