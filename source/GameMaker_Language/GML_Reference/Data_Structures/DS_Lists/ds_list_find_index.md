# ds_list_find_index

With this function you can check the given list for a value and the
position within the list for that value will be returned. Note that if
there are more than one entries in the list with the same value, the
position of any one of them may be returned, and that if the value does
not exist, then -1 will be returned. Note that the value can be an
array, which you can check with the function [ is_array()
](../../Variable_Functions/is_array) .

#### Syntax:

``` gml
ds_list_find_index(id, val);
```

|          |                                                                                                             |                            |
|----------|-------------------------------------------------------------------------------------------------------------|----------------------------|
| Argument | Type                                                                                                        | Description                |
| id       |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the list to use. |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | The value to find.         |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
pos = ds_list_find_index(list, "Player1");
```

The above code checks the list indexed in the variable "list" for the
value "Player1" and stores the returned position in the variable "pos".
