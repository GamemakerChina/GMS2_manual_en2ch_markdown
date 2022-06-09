# ds_map_exists

This function will return true if the specified key exists in the
(previously created) DS map , and false if it does not.

#### Syntax:

``` gml
ds_map_exists(id, key);
```

|          |                                                                                                          |                                       |
|----------|----------------------------------------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                                                     | Description                           |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the data structure to check |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | The key to check for                  |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !ds_map_exists(inventory, "potions")
{
    ds_map_add(inventory, "potions", 1);
}
```

The above code will check the DS map indexed in the variable "inventory"
for the key "potions" and if it doesn't exist it will add it to the map.
