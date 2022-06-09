# ds_queue_copy

This function can be used to copy the contents of one queue into
another. Note that this does *NOT* remove the contents from the original
queue, nor does it destroy the original queue. When using this function
the queue being copied to must have been previously created and if it
contained any items before the copy, then these will be cleared first
(meaning this information will be lost).

#### Syntax:

``` gml
ds_queue_copy(id, source);
```

|          |                                                                                                                |                                  |
|----------|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                                                           | Description                      |
| id       |  [DS Queue ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Queues/ds_queue_create)  | The id of the new queue.         |
| source   |  [DS Queue ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Queues/ds_queue_create)  | The original queue to copy from. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
with (instance_create_layer(x, y, "Enemies", obj_Enemy))
{
    queue = ds_queue_create();
    ds_queue_copy(queue, other.queue);
}
```

The above function creates a new instance and then in that instance it
creates a new DS queue and copies the contents of the queue in the
instance running the code block, into the newly created instance queue.
