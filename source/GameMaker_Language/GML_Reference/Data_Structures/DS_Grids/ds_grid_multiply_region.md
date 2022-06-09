# ds_grid_multiply_region

With this function you can specify a region of the grid in which to
multiply each cell value by a given amount. ** NOTE ** This function
will only work with real numbers, not strings.

#### Syntax:

``` gml
ds_grid_multiply_region(index, x1, y1, x2, y2, val);
```

|          |                                                                                                             |                                                         |
|----------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Argument | Type                                                                                                        | Description                                             |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid.                                  |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the left of the region in the grid.   |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the top of the region in the grid.    |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the right of the region in the grid.  |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the bottom of the region in the grid. |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The value to multiply with the region cells.            |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_grid_multiply_region(mygrid, 5, 5, 10, 10, 2);
```

The above code will take all the values found within the defined
rectangular grid area and multiply each one by 2.
