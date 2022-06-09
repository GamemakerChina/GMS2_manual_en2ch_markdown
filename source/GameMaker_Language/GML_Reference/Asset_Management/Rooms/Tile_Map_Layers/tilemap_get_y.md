# tilemap_get_y

Using this function you can retrieve the y position (within the room) of
the tile map element. You give the tile map element ID (which you get
when you create a tile map element using [ layer_tilemap_create()
](layer_tilemap_create) or when you use the function [
layer_tilemap_get_id() ](layer_tilemap_get_id) ), and the function
will return the y-axis position.

#### Syntax:

``` gml
tilemap_get_y(tilemap_element_id);
```

|                    |                                                                                                                                             |                                                                      |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                                          |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tile map element to get the y position of |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_Walls"); var map_id = layer_tilemap_get_id(lay_id); var _x = tilemap_get_x(map_id); var _y = tilemap_get_y(map_id); tilemap_x(map_id, _x + 10); tilemap_y(map_id, _y + 10);
```

The above code uses the retrieved tile map ID to get the tile x and y
position of the tile map and then uses those values to move it.
