# ds_priority_clear

With this function you can clear all data from the given priority queue
data-structure. This does *NOT* destroy the data-structure (for that you
should use [ ds_priority_destroy() ](ds_priority_destroy) ) it only
wipes all data from it and returns an empty priority queue.

#### Syntax:

``` gml
ds_priority_clear(id);
```

|          |                                                                                                                               |                                        |
|----------|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                                          | Description                            |
| id       |  [DS Priority ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Priority_Queues/ds_priority_create)  | The id of the data structure to clear. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (count = 15) &amp;amp;&amp;amp; (!ds_priority_empty(command_queue))
{
    ds_priority_clear(command_queue);
    alarm[0] = room_speed;
    ai_count = 0;
}
```

The above code checks a variable to see if it has reached a specific
value and if it has it clears the DS priority queue indexed in the
variable "command_queue", sets an alarm, and resets the variable to 0.
