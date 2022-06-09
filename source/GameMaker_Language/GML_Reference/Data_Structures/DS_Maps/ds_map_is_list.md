# ds_map_is_list

With this function you can check to see if a [DS
list](../DS_Lists/DS_Lists) is stored in the given map key. If the
given key contains a DS list ID, then the function will return true
otherwise it will return false . Note that this will only detect lists
that were added using the [ds_map_add_list()](ds_map_add_list)
function.

#### Syntax:

``` gml
ds_map_is_list(id, key)
```

|          |                                                                                                          |                           |
|----------|----------------------------------------------------------------------------------------------------------|---------------------------|
| Argument | Type                                                                                                     | Description               |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map to use. |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | The key to check.         |

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
    if ds_map_is_list(inventory, key)
    {
        ds_list_destroy(inventory[? key]);
    }
    key = ds_map_find_next(inventory);
}
ds_map_destroy(inventory);
```

The above code loops through a DS map and checks to see if any of the
keys within it are for a DS list. If they are, then the DS list is
destroyed, and the at the end of the loop the DS map is destroyed too.
