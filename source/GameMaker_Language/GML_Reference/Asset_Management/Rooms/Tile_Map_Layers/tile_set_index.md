# tile_set_index

This function can be used to set the tile index (the position of the
tile within the tile set image) for a set of tile-data. You give the
tile-data, which can be retrieved using the function [ tilemap_get()
](tilemap_get) , and then the integer value that represents the
position of the tile (its index) within the tile set. The function will
return a modified tile-data set which can then be applied using the [
tilemap_set() ](tilemap_set) function.

#### Syntax:

``` gml
tile_set_index(tiledata, index)
```

|          |                                                                                                                          |                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                                                                     | Description                                |
| tiledata |  [Tile Data](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get)  | the tile-data to set                       |
| index    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                | The integer index value of the tile to use |

#### Returns:

``` gml
 Tile Data
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_sky");
var map_id = layer_tilemap_get_id(lay_id);
var mx = tilemap_get_cell_x_at_pixel(map_id, mouse_x, mouse_y);
var my = tilemap_get_cell_y_at_pixel(map_id, mouse_x, mouse_y);
var data = tilemap_get(map_id, mx, my);
var ind = tile_get_index(data);
data = tile_set_index(data, irandom(23));
tilemap_set(map_id, data, mx, my);
```

The above code gets the tile map ID from the given layer and then uses
that to get the tile-data for the cell under the mouse position. This
data is then used to set the tile index to a random number.
