# ds_map_is_map

With this function you can check to see if a DS map is stored in the
given map key. If the given key contains a DS map ID, then the function
will return true otherwise it will return false . Note that this will
only detect maps that were added using the
[ds_map_add_map()](ds_map_add_map) function.

#### Syntax:

``` gml
ds_map_is_map(id, key)
```

|          |                                                                                                          |                           |
|----------|----------------------------------------------------------------------------------------------------------|---------------------------|
| Argument | Type                                                                                                     | Description               |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map to use. |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | The key to replace.       |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var size = ds_map_size(inventory);
var key = ds_map_find_first(inventory);
for (var i = 0; i &amp;lt; size; i++)
{
    if ds_map_is_map(inventory, key)
    {
        ds_map_destroy(inventory[? key]);
    }
    key = ds_map_find_next(inventory);
}
ds_map_destroy(inventory);
```

The above code loops through a DS map and checks to see if any of the
keys within it are for other DS maps. If they are, then the stored DS
map is destroyed, and the at the end of the loop the main DS map is
destroyed too.
