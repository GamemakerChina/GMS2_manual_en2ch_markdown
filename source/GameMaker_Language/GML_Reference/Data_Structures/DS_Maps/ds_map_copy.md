# ds_map_copy

You can use this function to copy the contents of one map into another
one that you have previously created using
[ds_map_create()](ds_map_create) . If the DS map that is being
copied *to* is not empty, then this function will clear it first before
copying. The original DS map remains unchanged by this process.

#### Syntax:

``` gml
ds_map_copy(id, source);
```

|          |                                                                                                          |                                            |
|----------|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                                                     | Description                                |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map you are copying **to**   |
| source   |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map you are copying **from** |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
inventory_2 = ds_map_create(); ds_map_copy(inventory_2, inventory_1);
```

The above code will create a new map and assign it to the variable
"inventory_2". It will then copy the contents of the DS map indexed in
the variable "inventory_1" to this new map.
