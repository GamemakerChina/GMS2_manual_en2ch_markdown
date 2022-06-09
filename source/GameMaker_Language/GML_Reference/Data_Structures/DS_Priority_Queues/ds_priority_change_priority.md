# ds_priority_change_priority

This function will take a given value and change its priority within the
referenced priority queue. The given value should already exist in the
priority queue.

#### Syntax:

``` gml
ds_priority_change_priority(id, val, priority);
```

|          |                                                                                                                               |                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                                          | Description                             |
| id       |  [DS Priority ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Priority_Queues/ds_priority_create)  | The id of the priority queue to change. |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                                           | The value to change the priority of.    |
| priority |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                        | The new priority of the value.          |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (global.Game_Time &amp;lt; 1000)
{
    ds_priority_change(ai_priority, AI_Search, 1);
}
```

The above code checks a global variable and if it is below a certain
value it will then change the priority of the script function index held
in the priority queue.
