# ds_list_set

This function can be used to set a previously added list entry. You give
the list ID (as returned when you created the list) and the position
within the list to set as well as the value to set it to. Note that if
the entry being set is outside the bounds of the list (ie, you set list
entry 20 but the current list only contains 10 entries) then the list
will be filled to the given position and each entry will be set to 0.
This function is the same as using the [DS list
accessor](../../../GML_Overview/Accessors) .

#### Syntax:

``` gml
ds_list_set(id, pos, val);
```

|                       |                                                                                                             |                                      |
|-----------------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument              | Type                                                                                                        | Description                          |
| id                    |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the list to add to.        |
| pos                   |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | The position within the list to set. |
| \[val2, ... max_val\] |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | The value to set in the list.        |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
for (var i = 0; i &amp;lt; ds_list_size(list); i++;)
{
    ds_list_set(list, i, -1);
}
```

The above code will add the value stored in the "score" variable into
the list indexed in the variable "sc_list".
