# tilemap_set_width

This function can be used to resize a tile map element. You give the
tile map element ID (which you get when you create a tile map element
using [ layer_tilemap_create() ](layer_tilemap_create) or when you
use the function [ layer_tilemap_get_id() ](layer_tilemap_get_id) ),
and the new width of the tile map in tile cells.

#### Syntax:

``` gml
tilemap_set_width(tilemap_element_id, width)
```

|                    |                                                                                                                                             |                                                                 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                                     |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tile map element to set the width of |
| width              |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                   | The width value (in "cells")                                    |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_Walls");
var map_id = layer_tilemap_get_id(lay_id);
if tilemap_get_width(map_id) != room_width div 16
{
    tilemap_set_width(map_id, room_width div 16);
}
```

The above code checks the width of a specific tile map and if it is not
the correct size then the width is set.
