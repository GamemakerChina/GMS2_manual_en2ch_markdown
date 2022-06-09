# tilemap_get_global_mask

This function can be used to retrieve the bit mask value for *all* tile
maps, returning the current mask value or -1 if there is an error or 0
if no mask is specified. For further information on global tile map bit
masks, see the function [ tilemap_set_global_mask()
](tilemap_set_global_mask) .

#### Syntax:

``` gml
tilemap_get_global_mask();
```

#### Returns:

``` gml
 Real

(0 for no mask, -1 for an error, mask value otherwise)
```

#### Example:

``` gml
var mask = tilemap_get_global_mask(map_id);
var new_mask = tile_mirror | tile_flip | tile_rotate | 255;
if mask != new_mask
{
    tilemap_set_global_mask(new_mask);
}
```

The above code gets the global mask value associated with all tile maps.
If it is not the same as the value defined in the variable "new_mask",
then it is set to that value.
