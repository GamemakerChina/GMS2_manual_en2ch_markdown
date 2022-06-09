# ds_grid_add_grid_region

This function can be used to add all the values of all the cells found
within the source area of a grid to the values within the destination
grid, as illustrated below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Data_Structures/ds_grid_add_grid_region.png)  
** NOTE ** You can also use this function on the same grid to add values
from one region of the grid to those stored in another (see code example
below).

#### Syntax:

``` gml
ds_grid_add_grid_region(index, source, x1, y1, x2, y2, xpos, ypos);
```

|          |                                                                                                             |                                                                          |
|----------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Argument | Type                                                                                                        | Description                                                              |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the destination grid.                                       |
| source   |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the source grid.                                            |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The left position of the region of cells to copy from the source grid.   |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The top position of the region of cells to copy from the source grid.    |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The right position of the region of cells to copy from the source grid.  |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The bottom position of the region of cells to copy from the source grid. |
| xpos     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position on the destination grid to add the source region to.      |
| ypos     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position on the destination grid to add the source region to.      |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_grid_add_grid_region(grid, grid, 0, 0, 1, 5, 2, 0)
```

The above code would copy the region of cells from (0,0) to (1,5) of the
DS grid indexed in the variable "grid" and add them to the cells from
position (2,0) of the same DS grid .
