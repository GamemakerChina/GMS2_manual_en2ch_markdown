# ds_queue_enqueue

This function will add a value (real or string) onto the tail of the DS
queue . The function can take a further 14 optional arguments (making a
total of 15 possible additions), permitting you to add multiple values
consecutively to the tail of the queue in a single call.

#### Syntax:

``` gml
ds_queue_enqueue(id, val [, val2, ... val15]);
```

|                     |                                                                                                                |                                           |
|---------------------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument            | Type                                                                                                           | Description                               |
| id                  |  [DS Queue ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Queues/ds_queue_create)  | The id of the queue to add to.            |
| val                 |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                            | The value to add to the queue.            |
| \[val2, ... val15\] |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                            | Optional values to be added to the queue. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
move_queue = ds_queue_create(); ds_queue_enqueue(move_queue, x + 200); ds_queue_enqueue(move_queue, y); ds_queue_enqueue(move_queue, x + 200); ds_queue_enqueue(move_queue, y + 200); ds_queue_enqueue(move_queue, x); ds_queue_enqueue(move_queue,
y + 200); ds_queue_enqueue(move_queue, x); ds_queue_enqueue(move_queue, y);
```

The above code creates a new DS queue and stores its index in the
variable "move_queue". It then pushes a number of values onto the queue
for future use.
