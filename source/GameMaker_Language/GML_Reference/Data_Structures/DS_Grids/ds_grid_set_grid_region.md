# ds_grid_set_grid_region

This function can be used to copy the contents of a rectangular area of
grid cells from one (previously defined) DS grid to another, *or* it can
be used to copy a region from within the same grid. The following images
illustrate both ways that this function can be used:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Data_Structures/ds_grid_set_grid_region.png)  

#### Syntax:

``` gml
ds_grid_set_grid_region(index, source, x1, y1, x2, y2, xpos, ypos);
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
| xpos     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position on the destination grid to copy the source region to.     |
| ypos     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position on the destination grid to copy the source region to.     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_grid_set_grid_region(grid, t_grid, 0, 0, 5, 5, 10, 10)
```

This would copy the region of cells from (0,0) to (5,5) of the grid
indexed in the variable "t_grid" and copy them to position (10,10) in
the grid indexed in the variable "grid".
