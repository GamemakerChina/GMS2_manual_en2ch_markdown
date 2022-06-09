# ds_map_add_map

With this function you can assign a (previously created) DS map to a key
within the given DS map . This function is designed for creating JSON
compatible maps which you would then encode using [ json_encode()
](../../File_Handling/Encoding_And_Hashing/json_encode) and should
only be used in conjunction with that functionality. If a DS map has
another map added in this way, then destroying the parent map will also
destroy the contained maps and free their memory, and calling [
ds_map_clear() ](ds_map_clear) on the parent map will also destroy
and clean up any flagged maps.

#### Syntax:

``` gml
ds_map_add_map(id, key, value)
```

|          |                                                                                                          |                            |
|----------|----------------------------------------------------------------------------------------------------------|----------------------------|
| Argument | Type                                                                                                     | Description                |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map to use.  |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | The key for the added map. |
| value    |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map to add.  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var j_map = ds_map_create();
var j_list = ds_list_create();
var sub_map = ds_map_create();
ds_map_add_list(sub_map, "list", j_list);
ds_map_add(sub_map, "array", j_array);
ds_map_add_map(j_map, "map", sub_map);
var j = json_encode(j_map);
ds_map_destroy(j_map);
```

The above code will create two DS maps, and then populate one with a
list and an array before adding it into the second, which is then
encoded into a JSON string. The map is then destroyed to remove it, and
any other maps or lists that it contains, from memory.
