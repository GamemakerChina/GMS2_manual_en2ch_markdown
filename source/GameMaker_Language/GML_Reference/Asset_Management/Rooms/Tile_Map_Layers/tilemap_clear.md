# tilemap_clear

Using this function you can clear/set all the tiles on a given tile-map.
You give the tile map element ID (which you get when you create a tile
map element using [ layer_tilemap_create() ](layer_tilemap_create)
or when you use the function [ layer_tilemap_get_id()
](layer_tilemap_get_id) ), and then supply the tile data that you
wish to clear the layer with. A default value of 0 will clear all the
tiles from the layer (essentially making all tiles "empty"), while you
can use the dedicated tile\_\* functions to create your own tile data to
clear the tile map with.

#### Syntax:

``` gml
tilemap_clear(tilemap_element_id, tiledata)
```

|                    |                                                                                                                                             |                                                       |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                           |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tile map element to change |
| tiledata           |  [Tile Data](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get)                     | The tile data to use to clear the layer               |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var layer_id = layer_get_id("Forest");
var tile_id = layer_tilemap_get_id(layer_id);
tilemap_clear(tile_id, 0);
```

The above code gets the ID value of a tile map created in the room
editor, and then clears it using "empty" tiles.
