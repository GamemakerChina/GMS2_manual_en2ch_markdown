# ds_grid_destroy

This function will remove the given grid data-structure from memory,
freeing up the resources it was using and removing all values that it
contained. This function should always be used when you are finished
using the DS grid to prevent memory leaks that can slow down and crash
your game. **IMPORTANT!** When you create a data structure, the index
value to identify it is an integer value starting at 0. This means that
data structures of different types can have the **same** index value, so
if in doubt you should be using the [ ds_exists() ](../ds_exists)
function before accessing them. Also note that indices are re-used, so a
destroyed data structure index value may be used by a newly created one
afterwards so we recommend always setting the variable that held the DS
index to -1 after destroying.

#### Syntax:

``` gml
ds_grid_destroy(index);
```

|          |                                                                                                             |                                    |
|----------|-------------------------------------------------------------------------------------------------------------|------------------------------------|
| Argument | Type                                                                                                        | Description                        |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | This index of the grid to destroy. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (lives == 0)
{
    ds_grid_destroy(Wall_Grid);
    Wall_Grid = -1;
    room_goto(rm_Menu);
}
```

The above code will check the value of the built in global variable
"lives" and if it is 0, it destroys the DS grid indexed in the variable
"Wall_Grid" and then changes rooms.
