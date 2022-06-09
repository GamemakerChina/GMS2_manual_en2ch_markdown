# layer_tilemap_get_id

This function can be used to retrieve the unique ID value of the tile
map element on a layer. You supply the layer ID (which you get when you
create the layer using [ layer_create()
](../General_Layer_Functions/layer_create) ) or the layer name (as a
string - this will have a performance impact) and the function will
return the ID value associated with the tile map element on the layer.
Note that this function is specifically designed for use with tile maps
that have been added in the IDE, as if you add a tile map to a layer
through code using the function [ layer_tilemap_create()
](layer_tilemap_create) , then it will return the unique ID for the
tile map element added. If the given tilemap ID is incorrect or the
tilemap doesn't exist, the function will return -1.

#### Syntax:

``` gml
layer_tilemap_get_id(layer_id)
```

|          |                                                                                                                                                                                                                  |                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                                |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to target (or the layer name as a string) |

#### Returns:

``` gml
 Tile Map Element ID

or -1
```

#### Example:

``` gml
var lay_id = layer_get_id("tilemap_trees");
var tile_id = layer_tilemap_get_id(lay_id);
layer_tilemap_destroy(tile_id);
```

The above code will get the layer ID for the layer named "tilemap_trees"
and then use that to get the ID of the tile map element on that layer.
This ID is then used to remove the tile map from the layer.
