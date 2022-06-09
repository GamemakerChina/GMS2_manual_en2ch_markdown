# ds_list_mark_as_map

This function will "mark" (or "flag") a given position within a
previously created DS list as holding a [DS map](../DS_Maps/DS_Maps)
. This functionality is required when encoding JSON strings (which you
can create using [ json_encode()
](../../File_Handling/Encoding_And_Hashing/json_encode) ), but can
also be useful when nesting data-structures, as items marked in this way
will automatically be garbage collected (destroyed) when the parent DS
list is destroyed. This means that you do not have to manually go
through the list contents and destroy the marked data structures
individually before destroying the "parent" list. However, if you delete
the list position individually, the data structure it contained will
*not* be garbage collected and you should call the appropriate DS map
destroy function before deleting the parent list position. Also note
that if you call the function [ ds_list_clear() ](ds_list_clear) on
a list, any items flagged as maps will be destroyed as well when the
list is cleared. It is also worth noting that if the position that has
been marked changes within the list, the "mark" will move with it, so if
you have marked position 3 in the list (for example) and then insert 2
more items below it so it moves up to position 5, it will *still* be
marked as a map.

#### Syntax:

``` gml
ds_list_mark_as_map(id, pos);
```

|          |                                                                                                             |                                       |
|----------|-------------------------------------------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                                                        | Description                           |
| id       |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the list to mark.           |
| pos      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The position within the list to mark. |

#### Returns:

``` gml
 DS Map ID

or -1 (if it fails)
```

#### Example:

``` gml
var sub_map = ds_map_create();
ds_map_add(sub_map, "player", player_array);
ds_map_add(sub_map, "enemy", enemy_array);
ds_list_add(j_list, sub_map);
ds_list_mark_as_map(j_list, 0);
```

The above code creates a DS map and then populates it with two keys,
each containing an array of values. This map is then added into the
given DS list , and the position "marked" as such so that it can be
correctly encoded later.
