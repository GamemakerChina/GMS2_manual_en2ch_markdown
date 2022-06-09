# ds_list_replace

This function will replace the value at the given position for another
one.

#### Syntax:

``` gml
ds_list_replace(id, pos, val);
```

|          |                                                                                                             |                                                                                                                                           |
|----------|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                        | Description                                                                                                                               |
| id       |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the list to change.                                                                                                             |
| pos      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The position to replace the value, where 0 corresponds to the very beginning of the list and the final position is ds_list_size(id)-1 .   |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | The new value to replace the given value with.                                                                                            |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_list_replace(n_list, 3, name);
```

The above code will replace the value stored at position 3 in the list
for that stored in the variable "name".
