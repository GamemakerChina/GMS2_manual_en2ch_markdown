# ds_map_add_list

With this function you can assign a (previously created) [DS
list](../DS_Lists/DS_Lists) to a key within the given DS map. This
function is designed for creating JSON compatible maps which you would
then encode using [ json_encode()
](../../File_Handling/Encoding_And_Hashing/json_encode) and should
only be used in conjunction with that functionality. If a DS map has a
list added in this way, destroying the parent map will also destroy the
contained lists and free their memory, and calling [ ds_map_clear()
](ds_map_clear) on the parent map will also destroy and clean up any
flagged lists.

#### Syntax:

``` gml
ds_map_add_list(id, key, value)
```

|          |                                                                                                             |                             |
|----------|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| Argument | Type                                                                                                        | Description                 |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)     | The id of the map to use.   |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The key for the added list. |
| value    |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the list to add.  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var j_list = ds_list_create();
ds_list_add(j_list, health);
ds_list_add(j_list, lives);
ds_list_add(j_list, score);
var j_map = ds_map_create();
ds_map_add_list(j_map, "list", j_list);
var j = json_encode(j_map);
ds_map_destroy(j_map);
```

The above code will create a list and populate it with the various
values of global variables. This list is then "nested" within a DS map,
and the map is then encoded into a JSON string, before the map is
destroyed, removing it, and any lists it contains, from memory.
