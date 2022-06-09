# ds_priority_add

With this function you can add a value (either a real number or a
string) to a priority queue, at the same time assigning it a priority
value.

#### Syntax:

``` gml
ds_priority_add(id, val, priority);
```

|          |                                                                                                                               |                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                                          | Description                             |
| id       |  [DS Priority ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Priority_Queues/ds_priority_create)  | The id of the priority queue to add to. |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                                           | The value to add to the priority queue. |
| priority |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                        | The priority of the value to add.       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_priority_add(ai_priority, AI_Search, 5);
```

The above code adds a script function to the priority queue indexed in
the variable "ai_priority" and assigns it a priority of 5.
