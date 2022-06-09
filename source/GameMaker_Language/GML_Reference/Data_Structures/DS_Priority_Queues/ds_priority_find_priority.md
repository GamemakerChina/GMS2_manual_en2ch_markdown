# ds_priority_find_priority

With this function you can retrieve the priority of any given value. If
the value does not exist in the priority queue then undefined will be
returned.

#### Syntax:

``` gml
ds_priority_find_priority(id, val);
```

|          |                                                                                                                               |                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                                                                          | Description                          |
| id       |  [DS Priority ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Priority_Queues/ds_priority_create)  | The id of the priority queue to use. |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                                           | The value to find the priority of.   |

#### Returns:

``` gml
 Real

or

 undefined
```

#### Example:

``` gml
p = ds_priority_find_priority(ai_priority, "intelligence");
```

The above code will store the returned priority for the given value in
the instance variable "p".
