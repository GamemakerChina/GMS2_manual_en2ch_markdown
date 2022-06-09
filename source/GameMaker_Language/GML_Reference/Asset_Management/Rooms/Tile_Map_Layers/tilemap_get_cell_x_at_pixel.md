# tilemap_get_cell_x\_at_pixel

Using this function you can retrieve the x-axis position of an
individual tile map cell by giving the relative x-axis position within
the room. You give the tile map element ID (which you get when you
create a tile map element using [ layer_tilemap_create()
](layer_tilemap_create) or when you use the function [
layer_tilemap_get_id() ](layer_tilemap_get_id) ), as well as the x
and y position *within the room* and the function will return the x
position of the cell within the tile map for that point. Note that if
the value is outside of the tile map area, and no cell is available, it
will return -1.

#### Syntax:

``` gml
tilemap_get_cell_x_at_pixel(tilemap_element_id, x, y);
```

|                    |                                                                                                                                             |                                                                           |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                                               |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tile map element to get the cell x position of |
| x                  |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                   | The x position within the room to use for getting the cell                |
| y                  |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                   | The y position within the room to use for getting the cell                |

#### Returns:

``` gml
 Real

(x-axis cell position or -1 if there is an error)
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_Walls"); var map_id = layer_tilemap_get_id(lay_id); var _x = tilemap_get_cell_x_at_pixel(map_id, mouse_x, mouse_y); var _y = tilemap_get_cell_y_at_pixel(map_id, mouse_x, mouse_y); tiledata
= tilemap_get(map_id, _x, _y);
```

The above code uses the retrieved tile map ID to get the cell position
from a set of room coordinates and then store the data for any tile
found there in an instance variable.
