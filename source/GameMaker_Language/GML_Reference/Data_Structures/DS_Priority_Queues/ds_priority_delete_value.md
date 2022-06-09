# ds_priority_delete_value

This function will simply delete the given value, along with its
priority, from the indexed priority queue.

#### Syntax:

``` gml
ds_priority_delete_value(id,val);
```

|          |                                                                                                                               |                                              |
|----------|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                                          | Description                                  |
| id       |  [DS Priority ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Priority_Queues/ds_priority_create)  | The id of the priority queue to use.         |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                                           | The value to delete from the priority queue. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (ai_move == false)
{
    ds_priority_delete_value(ai_priority, AI_Move);
}
```

The above code checks an instance variable and if it returns false it
will remove the indexed script function from the priority queue.
