# tilemap_set_at_pixel

This function can be used to set a cell within the tile map element on
the layer to a new tile using the actual position of the tile to change
within the room. You give the tile map element ID (which you get when
you create a tile map element using [ layer_tilemap_create()
](layer_tilemap_create) or when you use the function [
layer_tilemap_get_id() ](layer_tilemap_get_id) ), and then the tile
data to set as well as the position within the room. You can retrieve
tile data using the function [ tilemap_get_at_pixel()
](tilemap_get_at_pixel) and then use the tile\_ functions to change
it before setting it again using this function. The function will return
true if the tile was successfully set and false if there was an issue
and it wasn't set.

#### Syntax:

``` gml
tilemap_set_at_pixel(tilemap_element_id, tiledata, x, y)
```

|                    |                                                                                                                                             |                                                       |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                           |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tile map element to change |
| tiledata           |  [Tile Data](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get)                     | The tile set data to set                              |
| xcell              |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                   | The x position (in the room)                          |
| ycell              |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                   | The y position (in the room)                          |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_sky");
var map_id = layer_tilemap_get_id(lay_id);
var data = tilemap_get_at_pixel(map_id, 4, 4);
data = tile_set_flip(data, true);
tilemap_set_at_pixel(map_id, data, 4, 4);
```

The above code gets the ID for the tile map on the layer "Tiles_Sky" and
then uses that to get the data from the tile at position (4, 4). This
tile data is then flipped before being used to set the tile on the tile
map again.
