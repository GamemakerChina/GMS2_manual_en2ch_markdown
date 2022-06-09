# tilemap_get_mask

This function can be used to retrieve the bit mask value for the given
tile map. You give the tile map element ID (which you get when you
create a tile map element using [ layer_tilemap_create()
](layer_tilemap_create) or when you use the function [
layer_tilemap_get_id() ](layer_tilemap_get_id) ), and the function
will return the current mask value or -1 if there is an error or 0 if no
mask is specified. For further information on tile map bit masks, see
the function [ tilemap_set_mask() ](tilemap_set_mask) .

#### Syntax:

``` gml
tilemap_get_mask(tilemap_element_id);
```

|                    |                                                                                                                                             |                                                                |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                                    |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tile map element to get the mask of |

#### Returns:

``` gml
 Real

(0 for no mask, -1 for an error)
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_sky");
var map_id = layer_tilemap_get_id(lay_id);
var mask = tilemap_get_mask(map_id);
var new_mask = tile_mirror | tile_flip | tile_rotate | 255;
if mask != new_mask
{
    tilemap_set_mask(map_id, new_mask);
}
```

The above code gets the tile map ID from the given layer and then checks
the mask value associated with it. If it is not the same as the value
defined in the variable "new_mask", then it is set to that value.
