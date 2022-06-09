# ds_priority_delete_min

This function will return the value that has the lowest priority in the
queue and then remove the value (and priority) from the data structure.
If more than one value has the same priority, then any one of them could
be returned in any order, but all other values with the same priority
will still be in the queue.

#### Syntax:

``` gml
ds_priority_delete_min(id);
```

|          |                                                                                                                               |                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                                                                          | Description                          |
| id       |  [DS Priority ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Priority_Queues/ds_priority_create)  | The id of the priority queue to use. |

#### Returns:

``` gml
 Variable

(Data type stored in the priority)
```

#### Example:

``` gml
if ai_move
{
    script_execute(ds_priority_delete_min(ai_priority));
}
```

The above code checks an instance variable and if it returns true it
will execute a script function indexed in the priority queue with the
lowest priority value and then remove that script from the queue.
