# tilemap_y

This function controls the position along the y-axis of the room of the
asset tile map element on the layer. You give the tile map element ID
(which you get when you create a tile map element using [
layer_tilemap_create() ](layer_tilemap_create) or when you use the
function [ layer_tilemap_get_id() ](layer_tilemap_get_id) ), and
then set the y value to use (based on the room coordinates).

#### Syntax:

``` gml
tilemap_y(tilemap_element_id, y);
```

|                    |                                                                                                                                             |                                                       |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                           |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tile map element to change |
| y                  |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                   | The y position for the tile map                       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Asset_sky");
var map_id = layer_tilemap_get_id(lay_id);
tilemap_y(map_id, irandom(room_height));
```

The above code gets the ID value of the tile map asset assigned to the
layer "Asset_sky" and then sets its y position to a random value between
0 and the height of the room.
