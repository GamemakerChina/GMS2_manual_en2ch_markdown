# ds_grid_multiply_disk

This function will take all the values in a given disc-shaped region of
the DS grid, and multiply each one by the given amount. ** NOTE ** This
function will only work with real numbers, not strings.

#### Syntax:

``` gml
ds_grid_multiply_disk(index, xm, ym, r, val);
```

|          |                                                                                                             |                                                       |
|----------|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument | Type                                                                                                        | Description                                           |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid.                                |
| xm       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the disk on the grid.               |
| ym       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the disk on the grid.               |
| r        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The radius of the disk on the grid.                   |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The value to multiply the cells within the disk with. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_grid_multiply_disk(mygrid, 5, 5, 5, 2)
```

The above code will take all the values found within the circular grid
area and multiply each one by 2.
