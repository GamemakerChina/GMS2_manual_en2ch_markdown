# ds_map_replace_map

With this function you can replace a DS Map that has been stored in the
given "key" with another map that has been created previously. This
function is designed for creating JSON compatible maps which you would
then encode using [ json_encode()
](../../File_Handling/Encoding_And_Hashing/json_encode) and should
only be used in conjunction with that functionality.

#### Syntax:

``` gml
ds_map_replace_map(id, key, value)
```

|          |                                                                                                          |                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| Argument | Type                                                                                                     | Description                                                                        |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the ds_map to use.                                                       |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | The key to replace.                                                                |
| value    |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the ds_map to use to replace the one previously stored in the given key. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var temp_map = ds_map_create();
ds_map_add_list(temp_map, "list", j_list);
ds_map_add(temp_map, "array", j_array);
ds_map_replace_map(j_map, "maps", temp_map);
var j = json_encode(j_map);
ds_map_destroy(temp_map);
```

The above code will create a DS Map and populate it with an array and a
DS List before replacing a previously stored map in the DS Map "j_map".
