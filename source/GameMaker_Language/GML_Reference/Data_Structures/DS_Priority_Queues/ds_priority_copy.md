# ds_priority_copy

This function can be used to copy the contents of one priority queue
into another. Note that this does *NOT* remove the contents from the
original priority queue, nor does it destroy the original priority
queue. When using this function the priority queue being copied to must
have been previously created and if it contained any items before the
copy, then these will be cleared first (meaning this information will be
lost).

#### Syntax:

``` gml
ds_priority_copy(id, source);
```

|          |                                                                                                                               |                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Argument | Type                                                                                                                          | Description                                   |
| id       |  [DS Priority ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Priority_Queues/ds_priority_create)  | The id of the priority queue to copy *to* .   |
| source   |  [DS Priority ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Priority_Queues/ds_priority_create)  | The id of the priority queue to copy *from* . |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
with (instance_create_layer(x, y, "Enemies", obj_Enemy))
{
    p_queue = ds_priority_create();
    ds_priority_copy(p_queue, other.p_queue);
}
```

The above function creates a new instance and then in that instance it
creates a new DS priority queue and copies the contents of the priority
queue in the instance running the code block, into the newly created
instance priority queue.
