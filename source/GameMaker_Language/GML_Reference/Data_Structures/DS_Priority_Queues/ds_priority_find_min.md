# ds_priority_find_min

With this function you can find the value stored in the priority queue
with the lowest priority, and if more than one value has the same
priority then any one of them could be returned in any order. However,
unlike [ ds_priority_delete_min() ](ds_priority_delete_min) , this
function will not remove the value from the queue.

#### Syntax:

``` gml
ds_priority_find_min(id);
```

|          |                                                                                                                               |                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                                                                          | Description                          |
| id       |  [DS Priority ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Priority_Queues/ds_priority_create)  | The id of the priority queue to use. |

#### Returns:

``` gml
 Real

or

 String
```

#### Example:

``` gml
if ai_move
{
    script_execute(ds_priority_find_min(ai_priority));
}
```

The above code checks an instance variable and if it returns true it
will execute a script function indexed in the priority queue with the
lowest priority value.
