# ds_queue_dequeue

This function will *dequeue* the head value off of the DS queue,
removing it from the queue and returning the value to be stored in a
variable. If the queue is empty then the function will return the
constant undefined , otherwise it will return the value contained in the
queue.

#### Syntax:

``` gml
ds_queue_dequeue(id);
```

|          |                                                                                                                |                                      |
|----------|----------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                                                           | Description                          |
| id       |  [DS Queue ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Queues/ds_queue_create)  | The id of the queue to dequeue from. |

#### Returns:

``` gml
 Variable

(Data type value stored in the queue) or

 undefined
```

#### Example:

``` gml
if !ds_queue_empty(move_queue)
{
    var xx = ds_queue_dequeue(move_queue);
    var yy = ds_queue_dequeue(move_queue);
    move_towards_point(xx, yy, 4);
}
```

The above code checks the DS queue indexed in the variable "move_queue"
to see if it is empty, and if it is not, it then dequeues the two values
from the head of the queue and use them to set a direction for movement.
