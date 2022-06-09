# ds_exists

With this function you can check to see if a data structure of the given
type exists. You supply the "index" value (as held in a variable) and
the DS "type", which can be any of the constants listed below, and the
function will return true if the data structure exists and false
otherwise.

|                                                                                                  |                                                                        |
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
|  [DS Type Constant](../../../../GameMaker_Language/GML_Reference/Data_Structures/ds_exists)  |                                                                        |
| Constant                                                                                         | Description                                                            |
|  ds_type_map                                                                                     | A [map](DS_Maps/DS_Maps) data structure                            |
|  ds_type_list                                                                                    | A [list](DS_Lists/DS_Lists) data structure                         |
|  ds_type_stack                                                                                   | A [stack](DS_Stacks/DS_Stacks) data structure                      |
|  ds_type_grid                                                                                    | A [grid](DS_Grids/DS_Grids) data structure                         |
|  ds_type_queue                                                                                   | A [queue](DS_Queues/DS_Queues) data structure                      |
|  ds_type_priority                                                                                | A [priority](DS_Priority_Queues/DS_Priority_Queues) data structure |

NOTE You cannot use this function to check the type of a data structure,
as the same index number may be used by multiple data structures of
differing types.

#### Syntax:

``` gml
ds_exists(ind, type);
```

|          |                                                                                                  |                                                                           |
|----------|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Argument | Type                                                                                             | Description                                                               |
| ind      |  [Any DS ID](../../../../GameMaker_Language/GML_Reference/Data_Structures/Data_Structures)   | The variable index to check for the data structure                        |
| type     |  [DS Type Constant](../../../../GameMaker_Language/GML_Reference/Data_Structures/ds_exists)  | The type of data structure to check for (see the list of constants above) |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !ds_exists(ai_grid, ds_type_grid)
{
    ai_grid = ds_grid_create(room_width / 32, room_height / 32);
}
```

The above code checks the (previously initialised) variable "ai_grid" to
see if it indexes a DS grid type data structure, and if it does not then
it creates one and stores its index in the variable.
