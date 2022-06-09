# ds_grid_add_disk

This function can be used to add a given value (real or string) to all
the values of the cells found within the defined disk area of a grid.
The value to be added must be of the same type as that held within the
grid cells, ie: you cannot add a string to a real or vice-versa, and for
strings this corresponds to concatenation.

#### Syntax:

``` gml
ds_grid_add_disk(index, xm, ym, r, val);
```

|          |                                                                                                             |                                                |
|----------|-------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| Argument | Type                                                                                                        | Description                                    |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid.                         |
| xm       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the disk on the grid.        |
| ym       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the disk on the grid.        |
| r        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The radius of the disk on the grid.            |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | The value to add to the cells within the disk. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_grid_add_disk(grid, 7, 6, 5, 2)
```

This would add 2 to all the values held in the cells within the defined
disk area of the DS grid referenced by the variable "grid".
