# draw_tilemap

This function can be used to draw a given tilemap anywhere in the room.
You give the tilemap element ID (which you get when you create a tilemap
element using [ layer_tilemap_create()
](../../Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_create)
or when you use the function [ layer_tilemap_get_id()
](../../Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)
), then give the x/y position for drawing (in the room). Note that this
will simply draw the tilemap at the specified point, using the layer
depth of the instance that is calling the function. It does *not* move
the tilemap - nor change it in any way - and does not matter if the
tilemap is flagged as visible or not.

#### Syntax:

``` gml
draw_tilemap(tilemap_element_id, x, y);
```

|                    |                                                                                                                                          |                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| Argument           | Type                                                                                                                                     | Description                                        |
| tilemap_element_id |  [Tile Map Element ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tilemap element to draw |
| x                  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                   | The x position within the room to draw at          |
| y                  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                   | The y position within the room to draw at          |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_Effects");
var map_id = layer_tilemap_get_id(lay_id);
draw_tilemap(map_id, mouse_x, mouse_y);
```

The above code gets the layer ID then uses that to get a specific
tilemap ID which in turn is used to draw the tilemap at the mouse's
position.
