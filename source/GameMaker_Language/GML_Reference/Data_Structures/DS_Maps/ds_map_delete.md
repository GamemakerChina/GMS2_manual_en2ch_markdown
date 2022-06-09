# ds_map_delete

With this function you can remove any given key (and its corresponding
value) from the given, previously created, DS map .

#### Syntax:

``` gml
ds_map_delete(id, key);
```

|          |                                                                                                          |                                                      |
|----------|----------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| Argument | Type                                                                                                     | Description                                          |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map to change.                         |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | The key to delete (along with its associated value). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_map_delete(inventory, "shield");
```

The above code will delete the key "shield" (and the value it is paired
with) from the DS map (inventory).
