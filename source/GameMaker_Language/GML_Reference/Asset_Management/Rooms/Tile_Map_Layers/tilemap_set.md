# tilemap_set

This function can be used to set any cell (grid square) within the tile
map element on the layer to a new tile. You give the tile map element ID
(which you get when you create a tile map element using [
layer_tilemap_create() ](layer_tilemap_create) or when you use the
function [ layer_tilemap_get_id() ](layer_tilemap_get_id) ), and
then the tile data to set as well as the position within the tile map.
You can retrieve tile data using the function [ tilemap_get()
](tilemap_get) and then use the tile\_ functions to change it before
setting the cell using this function. The function will return true if
the tile was successfully set and false if there was an issue and it
wasn't set.

#### Syntax:

``` gml
tilemap_set(tilemap_element_id, tiledata, xcell, ycell)
```

|                    |                                                                                                                                             |                                                       |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                           |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tile map element to change |
| tiledata           |  [Tile Data](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get)                     | The tile data to set                                  |
| xcell              |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                   | The cell (grid) position to set along the x-axis      |
| ycell              |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                   | The cell (grid) position to set along the y-axis      |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_sky");
var map_id = layer_tilemap_get_id(lay_id);
var data = tilemap_get(map_id, 0, 0);
data = tile_set_flip(data, true);
tilemap_set(map_id, data, 0, 0);
```

The above code gets the ID for the tile map on the layer "Tiles_Sky" and
then uses that to get the data from the tile at cell (0, 0). This tile
data is then flipped before being used to set the tile on the tile map
again.
