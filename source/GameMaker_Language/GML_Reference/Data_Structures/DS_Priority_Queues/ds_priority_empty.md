# ds_priority_empty

With this function you can check the given DS priority queue to see if
it is empty (returns true ) or not (returns false ).

#### Syntax:

``` gml
ds_priority_empty(id);
```

|          |                                                                                                                               |                                        |
|----------|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                                          | Description                            |
| id       |  [DS Priority ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Priority_Queues/ds_priority_create)  | The id of the data structure to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if (count == 15) &amp;amp;&amp;amp; (!ds_priority_empty(command_queue))
{
    ds_priority_clear(command_queue);
    alarm[0] = room_speed;
    ai_count = 0;
}
```

The above code checks a variable to see if it has reached a specific
value and if it has it clears the DS priority queue indexed in the
variable "command_queue", sets an alarm, and resets the variable to 0.
