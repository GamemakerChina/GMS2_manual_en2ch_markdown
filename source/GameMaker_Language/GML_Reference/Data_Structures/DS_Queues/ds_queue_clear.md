# ds_queue_clear

With this function you can clear all data from the given queue
data-structure. This does *NOT* destroy the data-structure (for that you
should use [ ds_queue_destroy() ](ds_queue_destroy) ) it only wipes
all data from it and returns an empty queue.

#### Syntax:

``` gml
ds_queue_clear(id);
```

|          |                                                                                                                |                                        |
|----------|----------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                           | Description                            |
| id       |  [DS Queue ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Queues/ds_queue_create)  | The id of the data structure to clear. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (count = 15) &amp;amp;&amp;amp; (!ds_queue_empty(command_queue))
{
    ds_queue_clear(command_queue);
    alarm[0] = room_speed;
    ai_count = 0;
}
```

The above code checks a variable to see if it has reached a specific
value and if it has it clears the DS queue indexed in the variable
"command_queue", sets an alarm, and resets the variable to 0.
