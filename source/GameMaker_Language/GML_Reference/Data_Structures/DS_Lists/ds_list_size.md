# ds_list_size

This function will return the "size" of the list, ie: the number of
items that have been added into it.

#### Syntax:

``` gml
ds_list_size(id);
```

|          |                                                                                                             |                                        |
|----------|-------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                        | Description                            |
| id       |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the data structure to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if !ds_list_empty(control_list)
{
    num = ds_list_size(control_list);
}
```

The above code checks a DS list to see if it is empty or not, and if it
is not, it gets the number of items that it contains and stores the
value in a variable.
