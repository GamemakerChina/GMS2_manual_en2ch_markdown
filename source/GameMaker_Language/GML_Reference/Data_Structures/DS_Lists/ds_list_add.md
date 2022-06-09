# ds_list_add

This function can be used to add a new value (real or string) to the
list, which will be added on at the end. The function can take further
optional arguments (as many as you require), permitting you to add
multiple values consecutively to the list in a single call.

#### Syntax:

``` gml
ds_list_add(id, val1 [, val2, ... max_val]);
```

|                       |                                                                                                             |                                          |
|-----------------------|-------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Argument              | Type                                                                                                        | Description                              |
| id                    |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the list to add to.            |
| val                   |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | The value to add to the list.            |
| \[val2, ... max_val\] |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | Optional values to be added to the list. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_list_add(sc_list, score);
```

The above code will add the value stored in the "score" variable into
the list indexed in the variable "sc_list".
