# ds_map_replace_list

With this function you can replace a [DS list](../DS_Lists/DS_Lists)
that has been stored in the given "key" with another list that has been
created previously. This function is designed for creating JSON
compatible maps which you would then encode using [ json_encode()
](../../File_Handling/Encoding_And_Hashing/json_encode) and should
only be used in conjunction with that functionality.

#### Syntax:

``` gml
ds_map_replace_list(id, key, value)
```

|          |                                                                                                             |                                                                                     |
|----------|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| Argument | Type                                                                                                        | Description                                                                         |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)     | The id of the map to use.                                                           |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The key to replace.                                                                 |
| value    |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the ds_list to use to replace the one previously stored in the given key. |

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
ds_map_replace_list(j_map, "list", j_list);
var j = json_encode(j_map);
ds_list_destroy(j_list);
```

The above code will create a DS List and populate it with the values of
various global variables before replacing a previously stored list in
the DS Map "j_map".
