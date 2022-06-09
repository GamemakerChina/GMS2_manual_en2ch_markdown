# layer_tilemap_create

With this function you can assign a tile-set resource to a layer to be
used as a tile map in your project. You supply the layer ID (which you
get when you create the layer using [ layer_create()
](../General_Layer_Functions/layer_create) ) or the layer name (as a
string - this will have a performance impact) and then an initial (x, y)
position to add the tile map to the room, the tile set resource to use,
and then the width and height of the tile map in *cells* (ie: a width of
20 and a height of 10 will create a tile map with 200 cells that is 20
cells wide and 10 cells tall), with the size of the cells themselves
being defined by the tile set chosen. It is worth noting that you cannot
place tiles at negative positions within the tile map, so all tiles must
be placed within the cell spaces 0 to width - 1, 0 to height - 1.

#### Syntax:

``` gml
layer_tilemap_create(layer_id, x, y, tileset, width, height)
```

|          |                                                                                                                                                                                                                  |                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                                |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to target (or the layer name as a string) |
| x        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                        | The x position of the tile map in the room                                 |
| y        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                        | The y position of the tile map in the room                                 |
| tileset  |  [Tile Set Asset](../../../../../../The_Asset_Editors/Tile_Sets)                                                                                                                                             | The Tile Set asset to be used                                              |
| width    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                        | The width tile map (in cells)                                              |
| height   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                        | The height of the tile map (in cells)                                      |

#### Returns:

``` gml
 Tile Map Element ID
```

#### Example:

``` gml
global.back_layer = layer_create(10000);
global.back_tiles = layer_tilemap_create(global.back_layer, 0, 0, tmap_Trees, 16, 32);
```

The above code creates a new layer and then adds a new tile map element
to it, setting the tile map position to (0,0) as well as the tile set to
be used and the width and height of the tile map.
