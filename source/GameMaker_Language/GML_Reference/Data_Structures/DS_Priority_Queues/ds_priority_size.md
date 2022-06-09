# ds_priority_size

This function will return the "size" of the priority queue, ie: the
number of items that have been prioritized in it.

#### Syntax:

``` gml
ds_priority_size(id);
```

|          |                                                                                                                               |                                        |
|----------|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                                          | Description                            |
| id       |  [DS Priority ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Priority_Queues/ds_priority_create)  | The id of the data structure to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if !ds_priority_empty(control_priority)
{
    num = ds_priority_size(control_priority);
}
```

The above code checks a DS priority queue to see if it is empty or not,
and if it is not, it gets the number of items that it contains and
stores the value in a variable.
