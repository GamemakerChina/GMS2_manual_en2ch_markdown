# ds_list_clear

With this function you can clear all data from the given list
data-structure. This does *NOT* destroy the data-structure (for that you
should use [ ds_list_destroy() ](ds_list_destroy) ) it only wipes
all data from it and makes the list empty (zero in size). Note that
clearing a list will de-reference any data structures stored in it
giving a memory leak, so you would need to go through the list and
destroy all data structure items manually before clearing it to prevent
this. The only time this is not required is when you have flagged any
items in the list as another [DS list](DS_Lists) or as a [DS
map](../DS_Maps/DS_Maps) , in which case these items will be
destroyed (not cleared!) and their memory cleaned up automatically when
the parent is cleared.

#### Syntax:

``` gml
ds_list_clear(id);
```

|          |                                                                                                             |                                        |
|----------|-------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                        | Description                            |
| id       |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the data structure to clear. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (count == 15) &amp;amp;&amp;amp; (!ds_list_empty(command_list))
{
    ds_list_clear(command_list);
    alarm[0] = room_speed;
    ai_count = 0;
}
```

The above code checks a variable to see if it has reached a specific
value and if it has it clears the DS list indexed in the variable
"command_list", sets an alarm, and resets the variable to 0.
