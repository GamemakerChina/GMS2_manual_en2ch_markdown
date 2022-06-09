# tilemap_get_tile_height

Using this function you can retrieve the height (in pixels) of each tile
cell of the tile map element. You give the tile map element ID (which
you get when you create a tile map element using [
layer_tilemap_create() ](layer_tilemap_create) or when you use the
function [ layer_tilemap_get_id() ](layer_tilemap_get_id) ), and the
function will return the tile set cell height.

#### Syntax:

``` gml
tilemap_get_tile_height(tilemap_element_id);
```

|                    |                                                                                                                                             |                                                                            |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                                                |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tile map element to get the tile cell height of |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_Walls"); var map_id = layer_tilemap_get_id(lay_id); global.snap_x = tilemap_get_tile_width(map_id); global.snap_y = tilemap_get_tile_height(map_id);
```

The above code uses the retrieved tile map ID to get the tile cell width
and height and use them to set two global variables.
