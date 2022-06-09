# ds_queue_size

This function will return the "size" of the queue, ie: the number of
items that have been queued onto it.

#### Syntax:

``` gml
ds_queue_size(id);
```

|          |                                                                                                                |                                        |
|----------|----------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                           | Description                            |
| id       |  [DS Queue ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Queues/ds_queue_create)  | The id of the data structure to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if !ds_queue_empty(control_queue)
{
    num = ds_queue_size(control_queue);
}
```

The above code checks a DS queue to see if it is empty or not, and if it
is not, it gets the number of items that it contains and stores the
value in a variable.
