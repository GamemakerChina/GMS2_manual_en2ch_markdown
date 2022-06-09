# ds_list_sort

With this function you can sort all the values within a list, either in
ascending or descending order. If the list contains strings, these will
be sorted alphabetically, based on the English 26 letter alphabet.

#### Syntax:

``` gml
ds_list_sort(id, ascend);
```

|          |                                                                                                             |                                                                                    |
|----------|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| Argument | Type                                                                                                        | Description                                                                        |
| id       |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the list to sort.                                                        |
| ascend   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                   | Whether the values should be ascending ( true ) or descending ( false ) order.     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if newgame
{
    ds_list_sort(name_list, true);
}
```

The above code will sort the list indexed in the variable "name_list" if
the variable "newgame" is flagged as true .
