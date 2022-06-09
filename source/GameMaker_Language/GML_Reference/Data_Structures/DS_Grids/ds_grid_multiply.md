# ds_grid_multiply

This function will multiply the value of the given grid cell by the
specified amount. ** NOTE ** This function will only work with real
numbers, not strings.

#### Syntax:

``` gml
ds_grid_multiply(index, x, y, val);
```

|          |                                                                                                             |                                         |
|----------|-------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                        | Description                             |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid.                  |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the cell in the grid. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the cell in the grid. |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The value to multiply with the cell.    |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_grid_multiply(mygrid, 5, 5, 2)
```

The above code will multiply the value stored in the given DS grid cell
by 2.
