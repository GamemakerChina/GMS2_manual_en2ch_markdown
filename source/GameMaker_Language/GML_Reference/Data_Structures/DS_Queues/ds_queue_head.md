# ds_queue_head

This function will only *read* the first value of the queue (that which
is "at the head"). It will not *dequeue* the value, meaning that it can
still be read in the future by this function or the [ ds_queue_dequeue()
](ds_queue_dequeue) . If the queue is empty then the function will
return the constant undefined , otherwise it will return the real or
string value contained in the queue.

#### Syntax:

``` gml
ds_queue_head(id);
```

|          |                                                                                                                |                                            |
|----------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                                                           | Description                                |
| id       |  [DS Queue ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Queues/ds_queue_create)  | The id of the data structure to read from. |

#### Returns:

``` gml
 Variable

(Data type value stored in the queue)
```

#### Example:

``` gml
num = ds_queue_head(control_queue);
```

The above code will read the value from the queue indexed in the
variable "control_queue" and store the return value in the variable
"num".
