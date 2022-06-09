# ds_stack_empty

With this function you can check the given DS stack to see if it is
empty (returns true ) or not (returns false ).

#### Syntax:

``` gml
ds_stack_empty(id);
```

|          |                                                                                                                |                                        |
|----------|----------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                           | Description                            |
| id       |  [DS Stack ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Stacks/ds_stack_create)  | The id of the data structure to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if (ai_count == 15 &amp;amp;&amp;amp; !ds_stack_empty(AI_stack))
{
    ds_stack_clear(AI_stack);
    alarm[0] = room_speed;
    ai_count = 0;
}
```

The above code checks a variable to see if it has reached a specific
value and if it has it clears the DS stack indexed in the variable
"AI_stack", sets an alarm, and resets the variable to 0.
