# ds_list_empty

With this function you can check the given DS list to see if it is empty
(returns true ) or not (returns false ).

#### Syntax:

``` gml
ds_list_empty(id);
```

|          |            |                                        |
|----------|------------|----------------------------------------|
| Argument | Type       | Description                            |
| id       | DS List id | The id of the data structure to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if (count == 15( &amp;amp;&amp;amp; (!ds_list_empty(command_list))
{
    ds_list_clear(command_list);
    alarm[0] = room_speed;
    count = 0;
}
```

The above code checks a variable to see if it has reached a specific
value and if it has it clears the DS list indexed in the variable
"command_list", sets an alarm, and resets the variable to 0.
