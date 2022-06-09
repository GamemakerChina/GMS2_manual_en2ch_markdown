# tilemap_get_at_pixel

Using this function you can retrieve the tile data from a position
(within the room) of the tile map element. You give the tile map element
ID (which you get when you create a tile map element using [
layer_tilemap_create() ](layer_tilemap_create) or when you use the
function [ layer_tilemap_get_id() ](layer_tilemap_get_id) ) as well
as the x and y position *in the room* to get the tile data from and the
function will return the tile data "blob". This data is essentially a
bit mask that contains the tile index, the flip/rotate/mirror booleans
and any mask data that has been applied (see [ tilemap_set_mask()
](tilemap_set_mask) for details), and the resulting data value can
then be used in the tile\_\* functions to change a tiles properties. If
you need to get the tile data from a specific tile cell you should be
using the function [ tilemap_get() ](tilemap_get) instead.
**IMPORTANT!** If the tiles in the tile map have been unchanged (ie:
they are **not** rotated or flipped etc...), then the return value of
the tile set data will be exactly equal to the index of the tile on the
tile set. So you can create "collision maps" of tiles using one tile at
index 1 in the tile set - for example - then use this function to check
for 1 or 0 (an empty tile) to calculate collisions.

#### Syntax:

``` gml
tilemap_get_at_pixel(tilemap_element_id, x, y);
```

|                    |                                                                                                                                             |                                                                          |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                                              |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tile map element to get the tile-data of      |
| x                  |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                   | The position along the x-axis to get the tile data from (in room pixels) |
| y                  |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                   | The position along the y-axis to get the tile data from (in room pixels) |

#### Returns:

``` gml
 Tile Data

(-1 if there is an error)
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_sky");
var map_id = layer_tilemap_get_id(lay_id);
var data = tilemap_get_at_pixel(map_id, 64, 128);
data = tile_set_flip(data, true);
tilemap_set_at_pixel(map_id, data, 64, 128);
```

The above code gets the ID for the tile map "Clouds" on the layer
"Tiles_Sky" and then uses that to get the data from the tile at position
(64, 128). This tile data is then flipped before being used to set the
tile on the tile map again.
