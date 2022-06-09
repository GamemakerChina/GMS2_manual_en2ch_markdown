# ds_grid_add

This function can be used to add a given value (real or string) to the
value of the given cell within the grid. The value to be added must be
the same type as that held within the grid cell, ie: you cannot add a
string to a real or vice-versa, and for strings this corresponds to
concatenation.

#### Syntax:

``` gml
ds_grid_add(index, x, y, val);
```

|          |                                                                                                             |                                         |
|----------|-------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                        | Description                             |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid.                  |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the cell in the grid. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the cell in the grid. |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | The value to add to the cell.           |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_grid_add(grid, 5, 5, 6)
```

This would add 6 to the given cell within the DS grid referenced by the
variable "grid".
